# Script to Detect Duplicate Bookings Using HashMap

This script detects duplicate hotel bookings efficiently using a HashMap (dictionary in Python). It checks for duplicate bookings by looking for identical bookings based on user ID, hotel ID, and check-in/check-out dates.

## Python Script: Detect Duplicate Bookings

```python
# Function to detect duplicate bookings
def detect_duplicate_bookings(bookings):
    # Create a HashMap (dictionary) to store unique bookings
    booking_map = {}
    duplicates = []

    for booking in bookings:
        # Extract booking details (e.g., user_id, hotel_id, check-in date, check-out date)
        user_id = booking['user_id']
        hotel_id = booking['hotel_id']
        check_in_date = booking['check_in']
        check_out_date = booking['check_out']
        
        # Generate a unique key for the booking based on user_id, hotel_id, and booking dates
        booking_key = (user_id, hotel_id, check_in_date, check_out_date)
        
        # Check if the booking already exists in the map (indicating a duplicate)
        if booking_key in booking_map:
            duplicates.append(booking)
        else:
            booking_map[booking_key] = booking

    return duplicates


# Sample list of bookings (user_id, hotel_id, check-in, check-out)
bookings = [
    {'user_id': 1, 'hotel_id': 101, 'check_in': '2023-07-01', 'check_out': '2023-07-05'},
    {'user_id': 2, 'hotel_id': 102, 'check_in': '2023-07-02', 'check_out': '2023-07-06'},
    {'user_id': 1, 'hotel_id': 101, 'check_in': '2023-07-01', 'check_out': '2023-07-05'},  # Duplicate
    {'user_id': 3, 'hotel_id': 103, 'check_in': '2023-07-03', 'check_out': '2023-07-07'},
    {'user_id': 2, 'hotel_id': 102, 'check_in': '2023-07-02', 'check_out': '2023-07-06'}   # Duplicate
]

# Call the function to detect duplicates
duplicates = detect_duplicate_bookings(bookings)

# Print the detected duplicates
if duplicates:
    print("Duplicate Bookings Detected:")
    for duplicate in duplicates:
        print(duplicate)
else:
    print("No duplicate bookings found.")
