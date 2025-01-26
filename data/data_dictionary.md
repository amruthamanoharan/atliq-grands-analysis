# Data Dictionary

This document provides detailed descriptions of the datasets used in the Atliq Grands data analysis project.

---

## **dim_date.csv**
- **Description**: Contains date-related information for reference and analysis.
- **Columns**:
  - `date_id`: Unique identifier for each date.
  - `full_date`: The complete date (YYYY-MM-DD format).
  - `day_of_week`: Name of the day (e.g., Monday, Tuesday).
  - `week_number`: Week number of the year.
  - `month`: Month name (e.g., January, February).
  - `quarter`: Quarter of the year (e.g., Q1, Q2).
  - `year`: The year corresponding to the date.

---

## **dim_hotels.csv**
- **Description**: Contains details about Atliq Grands’ hotel properties.
- **Columns**:
  - `hotel_id`: Unique identifier for each hotel.
  - `hotel_name`: Name of the hotel (e.g., Atliq Palace, Atliq Bay).
  - `location`: City where the hotel is located (e.g., Delhi, Mumbai).
  - `category`: Hotel category (e.g., luxury, standard, budget).

---

## **dim_rooms.csv**
- **Description**: Provides information about room types and their features.
- **Columns**:
  - `room_id`: Unique identifier for each room type.
  - `room_type`: Type of room (e.g., Standard, Elite, Premium, Presidential).
  - `capacity`: Maximum occupancy of the room.
  - `rate_per_night`: Base rate for one night's stay (in INR).

---

## **fact_aggregated_bookings.csv**
- **Description**: Aggregated booking and revenue data for summary analysis.
- **Columns**:
  - `hotel_id`: Identifier for the associated hotel.
  - `date_id`: Identifier for the booking date.
  - `total_revenue`: Total revenue generated on the given date (in INR).
  - `total_bookings`: Total number of bookings.
  - `occupancy_rate`: Percentage of rooms occupied.

---

## **fact_bookings.csv**
- **Description**: Detailed transactional data for individual bookings.
- **Columns**:
  - `booking_id`: Unique identifier for each booking.
  - `hotel_id`: Identifier for the associated hotel.
  - `room_id`: Identifier for the room type booked.
  - `customer_type`: Type of customer (e.g., regular, VIP).
  - `booking_channel`: Booking medium (e.g., website, third-party, offline).
  - `check_in_date`: Customer's check-in date.
  - `check_out_date`: Customer's check-out date.
  - `total_nights`: Total number of nights booked.
  - `revenue`: Revenue generated from this booking (in INR).

---

## **new_data_august.csv**
- **Description**: Additional booking data collected for the month of August 2024.
- **Columns**:
  - Same structure as `fact_bookings.csv`.

---

## Notes
- **Key Identifiers**:
  - `date_id`, `hotel_id`, and `room_id` are used to join datasets.
- **Data Cleaning**:
  - Missing values and anomalies were handled during preprocessing.
- **Purpose**:
  - These datasets are used for analyzing revenue trends, booking patterns, and customer segmentation.
