---
layout: mechatronics
title: Autonomous Mechatronics Robot
permalink: /projects/mechatronics-robot/
---

<section class="mech-hero">
  <div class="mech-shell">
    <p class="mech-kicker">MAE 3780 · Mechatronics</p>
    <h1 class="mech-title">Autonomous Mechatronics Robot</h1>
    <p class="mech-lede">
      An autonomous mobile robot developed around sensing, embedded control, motor actuation, system integration, and passive cube collection. The robot used color sensing to recognize the field boundary, low level AVR programming to process sensor pulses, and differential motor control to navigate the competition field while gathering cubes within its perimeter.
    </p>

    <div class="mech-tags" aria-label="Project skills">
      <span class="mech-tag">Embedded C</span>
      <span class="mech-tag">Arduino Uno</span>
      <span class="mech-tag">AVR Registers</span>
      <span class="mech-tag">Interrupts</span>
      <span class="mech-tag">Timers</span>
      <span class="mech-tag">Color Sensing</span>
      <span class="mech-tag">Motor Control</span>
      <span class="mech-tag">System Integration</span>
    </div>

    <div class="mech-actions">
      <a class="mech-button" href="{{ '/assets/MAE-3780-Final-Technical-Report.pdf' | relative_url }}" target="_blank" rel="noopener">
        View Final Technical Report
      </a>
    </div>
  </div>
</section>

<section class="mech-section">
  <div class="mech-shell">
    <p class="mech-eyebrow">System Overview</p>
    <h2 class="mech-section-title">Sensing, control, collection, and motion in one autonomous system</h2>

    <div class="mech-system-grid">
      <div class="mech-copy">
        <p>
          The robot was built around an Arduino Uno, a TCS3200 color sensor, two DC motors, and motor driver electronics. The color sensor continuously measured the surface beneath the robot and supplied a pulse signal that the microcontroller timed directly using AVR hardware registers.
        </p>
        <p>
          Five sensor readings were averaged before each boundary decision. A calibrated threshold separated the black border from the rest of the playing field. This reduced sensitivity to individual readings and gave the control loop a simple, repeatable trigger for changing direction.
        </p>
        <p>
          Cube collection was handled mechanically while the electronics focused on navigation. The front guide geometry directed cubes toward openings along the sides of the robot, and the surrounding retention geometry helped keep collected cubes within the robot perimeter as it continued moving around the field.
        </p>
      </div>

      <div class="mech-specs">
        <div class="mech-spec">
          <div class="mech-spec-label">Controller</div>
          <div class="mech-spec-value">Arduino Uno with AVR register control</div>
        </div>
        <div class="mech-spec">
          <div class="mech-spec-label">Sensor</div>
          <div class="mech-spec-value">TCS3200 color sensor</div>
        </div>
        <div class="mech-spec">
          <div class="mech-spec-label">Actuation</div>
          <div class="mech-spec-value">Two independently driven DC motors</div>
        </div>
        <div class="mech-spec">
          <div class="mech-spec-label">Detection Logic</div>
          <div class="mech-spec-value">Averaged pulse width with calibrated threshold</div>
        </div>
        <div class="mech-spec">
          <div class="mech-spec-label">Timing</div>
          <div class="mech-spec-value">Timer1 and pin change interrupts</div>
        </div>
        <div class="mech-spec">
          <div class="mech-spec-label">Navigation</div>
          <div class="mech-spec-value">Boundary reaction with variable turn timing</div>
        </div>
      </div>
    </div>

    <figure class="mech-diagram mech-diagram-wide">
      <a href="{{ '/assets/images/mechatronics/mechatronics-electrical-schematic.png' | relative_url }}" target="_blank" rel="noopener">
        <img src="{{ '/assets/images/mechatronics/mechatronics-electrical-schematic.png' | relative_url }}" alt="Electrical schematic showing the Arduino Uno, TCS3200 color sensor, motor drivers, motors, and power connections">
      </a>
      <figcaption>
        <strong>Electrical schematic</strong>
        <span>Arduino Uno, TCS3200 color sensing, dual motor drivers, DC motors, and the 6 V power system.</span>
      </figcaption>
    </figure>

    <div class="mech-control-grid">
      <div class="mech-copy">
        <p>
          Rather than using a separate cube detection system, the robot continuously covered the field and collected cubes through its forward motion. The guide geometry funneled cubes into the robot perimeter, allowing the collection system to work passively while the sensor and controller concentrated on keeping the robot on the playing surface and moving through different areas of the board.
        </p>
        <p>
          When the border was detected, the controller stopped the robot, reversed away from the edge, rotated back into the field, moved forward, and then applied a variable additional turn. Changing the turn duration reduced the chance of repeating the same trajectory, which helped the robot reach different cube locations while connecting sensor calibration, interrupt based timing, decision logic, and motor commands in one loop.
        </p>
      </div>

      <figure class="mech-diagram mech-diagram-flow">
        <a href="{{ '/assets/images/mechatronics/mechatronics-control-flowchart.png' | relative_url }}" target="_blank" rel="noopener">
          <img src="{{ '/assets/images/mechatronics/mechatronics-control-flowchart.png' | relative_url }}" alt="Flowchart of the autonomous robot sensing and navigation control logic">
        </a>
        <figcaption>
          <strong>Control logic</strong>
          <span>Sensor sampling, boundary detection, recovery motion, and variable turn behavior.</span>
        </figcaption>
      </figure>
    </div>
  </div>
</section>

<section class="mech-section mech-code-section">
  <div class="mech-shell">
    <div class="mech-code-intro">
      <div>
        <p class="mech-eyebrow">Embedded Software</p>
        <h2 class="mech-section-title">Full robot control code</h2>
      </div>
      <div class="mech-copy">
        <p>
          The program directly configures AVR data direction registers, Timer1, and pin change interrupts to handle sensing and timing close to the hardware. The sensor routine measures pulse width, averages multiple samples, detects the black boundary, and coordinates the motor response.
        </p>
      </div>
    </div>

    <div class="mech-code-window">
      <div class="mech-code-toolbar">
        <span class="mech-code-title">robot_control.c</span>
        <span class="mech-code-note">Scroll to view full source</span>
      </div>
      <div class="mech-code-scroll">
{% highlight c %}
#include <Arduino.h>
#include <avr/io.h>
#include <avr/interrupt.h>
#include <util/delay.h>

// Variable used to store pulse width from color sensor
volatile unsigned int timer = 0;

// Threshold used to determine if color black is detected
// Color sensor was calibrated by printing sensor readings
// to the serial monitor and comparing the values it measured over
// black and rest of board (yellow/blue).
#define BLACK_THRESHOLD 4000

// Motor control functions
void drive_forward(void);
void drive_backward(void);
void turn_left(void);
void stop_robot(void);

// Color sensor functions
void initColor(void);
unsigned int getColor(void);
unsigned int avgColor(void);
unsigned char isBlack(void);
unsigned int randomTurnTime(void);

// ISR for pin change interrupt on PortB
ISR(PCINT0_vect)
{
  // If sensor output pin is HIGH
  if (PINB & (1 << PINB2)) {
    // Reset Timer1
    TCNT1 = 0;
  } else {
    // Store value of Timer1 when LOW
    timer = TCNT1;
  }
}

// Initialize color sensor, interrupts, timer
void initColor(void)
{
  // Set D10 = PB2 as input for color sensor output
  DDRB &= ~(1 << DDB2);   // D10 input
  // Set D13 = PB5 as output for LED
  DDRB |= (1 << DDB5);    // D13 LED

  // Pin change interrupts PortB, disable PB2 interrupt initially
  PCICR |= (1 << PCIE0);
  PCMSK0 &= ~(1 << PCINT2);

  // Clear Timer1
  TCCR1A = 0x00;
  TCCR1B = 0x00;
  TCCR1B |= (1 << CS10);

  // Enable global interrupts
  sei();
}

// Measure one pulse from color sensor
unsigned int getColor(void)
{
  timer = 0; // Reset timer value
  TCNT1 = 0; // Reset counter in Timer1

  PCMSK0 |= (1 << PCINT2); // Enable interrupt on D10
  _delay_ms(10); // Delay 0.1 for pulses
  PCMSK0 &= ~(1 << PCINT2); // Disable interrupt after taking meas

  return timer;
}

// Take five readings from sensor and find average
unsigned int avgColor(void)
{
  unsigned long sum = 0;

  // Repeat fives times
  for (unsigned char i = 0; i < 5; i++) {
    sum += getColor(); // Add sensor reading to current total
    _delay_ms(2); //Delay for readings
  }

  return sum / 5; // Return avg. value
}

// Detect if black
unsigned char isBlack(void)
{
  unsigned int val = avgColor(); // Get averaged reading from sensor

  if (val > BLACK_THRESHOLD) { // Value greater than threshold
    PORTB |= (1 << PORTB5);    // LED on = black
    return 1;                  // Return true
  } else {
    PORTB &= ~(1 << PORTB5);   // LED off = not black
    return 0;                  // Return false
  }
}

int main(void)
{
  // Initialize Arduino
  init();

  // Motor pins
  // D8 = PB0, D9 = PB1
  // D5 = PD5, D6 = PD6
  DDRB |= (1 << DDB0) | (1 << DDB1); // Set as outputs
  DDRD |= (1 << DDD5) | (1 << DDD6); // Set as inputs

  // Initialize color sensor sys
  initColor();

  while (1) // Infinite loop
  {
    drive_forward(); // Drive forward

    if (isBlack()) // Check for black
    {
      stop_robot(); // If black, stop robot
      _delay_ms(100); // Delay (tune)

      // Back up from border
      drive_backward(); // Back away from black border
      _delay_ms(350);  // for 350 ms

      stop_robot();  // Stop again
      _delay_ms(100); // For 100 ms

      // Turn around ~180 degrees
      turn_left();
      _delay_ms(950);   // Tune this for exact 180
      stop_robot();     // Stop again
      _delay_ms(100);   // Delay (tune)

      // Go forward for a few seconds
      drive_forward(); // Drive forward
      _delay_ms(300); // For 350 ms

      stop_robot(); // Stop robot
      _delay_ms(100); // For 100 ms

      // Random turn after clearing border
      turn_left();

      // Generate random turn time
      unsigned int t = randomTurnTime(); // Using Timer1
      for (unsigned int i = 0; i < t; i++) { // Turn for random amount of time
        _delay_ms(1);
      }

      stop_robot(); // Stop
      _delay_ms(100); // For 100 ms
    }

    _delay_ms(10); // Delay for loop
  }
}

// Generate the random turn time
unsigned int randomTurnTime(void)
{
  // If 950 ms ≈ 180 degrees,
  // this gives random turn time from 100 ms to 950 ms.
  // changing it to give random turn max less than 90 degrees =around 45 deg
  unsigned int r = TCNT1; // Using Timer1
  return 100 + (r % 350); // Value between 100 and 450 ms
}

// Drive forward
void drive_forward(void)
{
  // Left motor forward
  PORTB |= (1 << PORTB0);
  PORTB &= ~(1 << PORTB1);

  // Right motor forward
  PORTD |= (1 << PORTD5);
  PORTD &= ~(1 << PORTD6);
}

// Drive backward
void drive_backward(void)
{
  // Left motor backward
  PORTB &= ~(1 << PORTB0);
  PORTB |= (1 << PORTB1);

  // Right motor backward
  PORTD &= ~(1 << PORTD5);
  PORTD |= (1 << PORTD6);
}

// Turn left
void turn_left(void)
{
  // Left motor backward
  PORTB &= ~(1 << PORTB0);
  PORTB |= (1 << PORTB1);

  // Right motor forward
  PORTD |= (1 << PORTD5);
  PORTD &= ~(1 << PORTD6);
}

// Stop
void stop_robot(void)
{
  // Turn off left motor
  PORTB &= ~((1 << PORTB0) | (1 << PORTB1));
  // Turn off right motor
  PORTD &= ~((1 << PORTD5) | (1 << PORTD6));
}
{% endhighlight %}
      </div>
    </div>
  </div>
</section>