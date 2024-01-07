# Django Project: Reservation System

## Overview

This Django project is a simple reservation system that facilitates booking appointments and displays menu information.

### Views

- `home(request)`: Renders the `index.html` page.
- `about(request)`: Renders the `about.html` page.
- `reservations(request)`: Retrieves bookings for a specified date. Renders the `bookings.html` page with booking details.
- `book(request)`: Handles form submissions using `BookingForm`. Saves valid form data. Renders the `book.html` page.
- `menu(request)`: Retrieves menu data. Renders the `menu.html` page with menu information.
- `display_menu_item(request, pk=None)`: Displays specific menu items based on primary key (`pk`). Renders the `menu_item.html` page.
- `bookings(request)`: Handles POST requests to create new bookings. Checks for existing bookings on a given date and slot. Responds with existing bookings or creates a new booking. Returns booking data in JSON format.

### Directory Structure

- `views.py`: Contains view functions for handling HTTP requests.
- `.forms`: Includes form definitions (`BookingForm`).
- `.models`: Contains data models (`Menu` and `Booking`).
- `index.html`, `about.html`, `bookings.html`, `book.html`, `menu.html`, `menu_item.html`: HTML templates.

### Usage
- Access different views:
  - Home: `/`
  - About: `/about/`
  - Reservations: `/reservations/`
  - Booking: `/book/`
  - Menu: `/menu/`
  - Display Menu Item: `/menu/{pk}/`

## `book.html` Template

### Description

The `book.html` template is designed to facilitate the process of making a reservation through a form interface. It displays booking details and available time slots for reservations.

### Template Content

- A form for making reservations that includes fields for name and selecting reservation time.
- Display section for bookings on a specific date.
- JavaScript functionality for dynamically handling form submissions and displaying available time slots and existing bookings.

### Usage

- To make a reservation, fill in the required fields (name and reservation time) and click the "Reserve" button.
- Existing bookings for the selected date are displayed under "Bookings for [Selected Date]".
