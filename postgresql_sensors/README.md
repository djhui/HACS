# PostgreSQL Sensors for Home Assistant

This custom component allows you to create sensors in Home Assistant that fetch data from a PostgreSQL database.

## Installation

1. Open Home Assistant.
2. Navigate to HACS (Home Assistant Community Store).
3. Click on "Integrations".
4. Click the "+" button in the bottom right corner.
5. Search for "PostgreSQL Sensors" and install it.

## Configuration

After installation, you can add PostgreSQL sensors through the Home Assistant UI:

1. Go to Configuration > Integrations.
2. Click the "+" button to add a new integration.
3. Search for "PostgreSQL Sensors" and select it.
4. Fill in the required information:
   - Host: Your PostgreSQL server address
   - Port: Your PostgreSQL server port (default is 5432)
   - Database: The name of your database
   - Username: Your PostgreSQL username
   - Password: Your PostgreSQL password
   - SQL Query: The query to fetch your sensor data

## Adding Sensors

Once the integration is set up, you can add individual sensors:

1. Go to Configuration > Integrations.
2. Find the PostgreSQL Sensors integration and click "Configure".
3. Click "Add Sensor".
4. Fill in the sensor details:
   - Name: A name for your sensor
   - SQL Query: The specific query for this sensor
   - Column: The column name from the query result to use as the sensor state
   - Unit (optional): The unit of measurement for the sensor
   - Icon (optional): An MDI icon for the sensor (e.g., mdi:database)

## Example Configuration

Here's an example of how to set up a sensor:

- Name: Temperature Sensor
- SQL Query: SELECT temperature FROM weather_data ORDER BY timestamp DESC LIMIT 1
- Column: temperature
- Unit: °C
- Icon: mdi:thermometer

This would create a sensor that displays the most recent temperature from a weather_data table.

## Notes

- Ensure your PostgreSQL server is accessible from your Home Assistant instance.
- Complex queries may impact Home Assistant's performance. Keep your queries as simple and efficient as possible.
- This integration requires the `psycopg2-binary` package, which should be automatically installed with the component.

For more information or to report issues, please visit the [GitHub repository](https://github.com/your_username/ha-postgresql-sensors).
![QR Code](https://github.com/user-attachments/assets/5c74897a-e32a-4fcc-b41c-1fc0d76a2494)

