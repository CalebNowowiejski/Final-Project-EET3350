# Final-Project-EET3350
## Assignment Details
View [ProductDefinition.pdf](https://github.com/CalebNowowiejski/Final-Project-EET3350/blob/main/ProductDefinition.pdf)

## Team and Project Information

**Project:** Smart Plant Watering System

**Team Members:** Blaine Carner, Caleb Nowowiejski (Project Lead), Fiza Shaikh

**Meeting Times:**
- **Monday:** 2:20 PM – 3:55 PM
- **Wednesday (As Needed):** 2:20 PM – 3:55 PM

## Github Repository and Other Links

**Github:** [Final-Project-EET3350](https://github.com/CalebNowowiejski/Final-Project-EET3350/tree/main)

**Wokwi:** [Wokwi](https://wokwi.com/projects/new/esp32-s2)

## Chosen Project and Minimum Viable Product

The project our team selected is the **Smart Plant Watering System**. This system measures the moisture level of a plant's soil and determines whether the plant requires water, eliminating the constant need for manual watering. It will also include built-in logic to prevent both overwatering and underwatering. The system is primarily designed for homeowners with small potted plants, making it easier to maintain their plants' health while reducing the amount of manual work required. The only regular maintenance required from the user is ensuring that the water container is refilled when necessary. To assist with this, the system will monitor the water level and notify the user when the container needs to be refilled by displaying a red LED. This significantly reduces the effort required to properly care for plants. The essential components of the minimum viable product include an available power outlet, an ESP32 microcontroller, a water container, tubing, a soil moisture sensor, a water pump, and the necessary wiring. Potential improvements to the project could include wireless notifications, a display showing real-time soil moisture readings, customizable watering settings based on the type of plant, and the ability to monitor and water multiple plants using a single system.

## Team Feedback and Improvements

The original project idea has remained mostly unchanged. As a group, we discussed how the system would function and what components would be necessary. The main area we are still deciding on is the best method for transferring water from the container into the soil. We plan to explore different approaches to determine which would work best for our system. So far, we believe a wired water pump is the best approach. In the future, we would also like to implement a couple features: a feature that allows the microcontroller to send text message notifications to the user when the water container is empty and needs to be refilled and a feature that allows multiple plants to be tracked at the same time.

## Concept Block Diagram and Firmware Behavior

## Updated AI Concept Rendering

## User Story, Tests, and Risks

**User Story:** As a homeowner with potted plants, I want an automated system that monitors soil moisture and waters my plants when necessary, so that I can keep my plants healthy without having to manually water them every day.

**Normal Operation Test:** The system starts with the water container filled and the soil moisture level below the acceptable range. The microcontroller requests a reading from the moisture sensor and determines that the soil is dry. It then activates the water pump to begin watering the plant while continuously monitoring the moisture level. Once the moisture reaches an acceptable level, the pump turns off, and the system records the time of watering. The test passes if the pump activates when the soil is dry, shuts off when the desired moisture level is reached, and successfully records the watering time.

**Exception Operation Test:** The system starts with dry soil and an empty water container. The microcontroller detects that the soil needs water and activates the water pump. However, the moisture level does not increase because no water is available. After a set amount of time without detecting an increase in moisture, the microcontroller should automatically shut off the pump to prevent damage and record an error. The test passes if the system detects the issue, shuts off the pump, and prevents further watering attempts until the problem is resolved. The test fails if the system does not detect the issue and allows the pump to continue running indefinitely while waiting for the desired moisture level to be reached.

**Failed Operation Test:** The system starts with dry soil and a full water container. The microcontroller requests a reading from the moisture sensor, but the sensor malfunctions and incorrectly reports that the soil has an acceptable moisture level. Because of this incorrect reading, the microcontroller does not activate the water pump, even though the plant requires water. The system continues operating normally without detecting or reporting an issue. The test fails because the plant does not receive the necessary water, and the system does not recognize that a malfunction has occurred.

**Technical and Safety Risks:** The main safety risk with this system is the combination of water and electricity. It is important to ensure that water cannot come into contact with the microcontroller, power outlet, or other electronic components. To test this, we can inspect the system for potential leaks and ensure all electrical components are properly protected. Another risk is the system failing to correctly water the plants, potentially causing them to become overwatered or underwatered. To test this, we can simulate different failures, such as an empty water container or a malfunctioning moisture sensor, and observe whether the system properly detects and responds to these issues.

## Schedule and Progress Checklist
- Updated AI Concept
- Block Diagram
- Progress Checklist for next assigment
