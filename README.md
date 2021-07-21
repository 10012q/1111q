month = input()
numbers_of_nights = int(input())
studio = 0
apartment = 0
if month in "May October":
    studio = 50 * numbers_of_nights
    apartment = 65 * numbers_of_nights
elif month in "June September":
    studio = 75.20 * numbers_of_nights
    apartment = 68.70 * numbers_of_nights
elif month in "July August":
    studio = 76 * numbers_of_nights
    apartment = 77 * numbers_of_nights

if numbers_of_nights >= 14:
    apartment = apartment - (apartment * 0.1)

if 7 >= numbers_of_nights <= 14 and month in "May October":
    studio = studio - (studio * 0.05)
if numbers_of_nights > 14 and month in "May October":
    studio = studio - (studio * 0.3)
if numbers_of_nights > 14 and month in "June September":
    studio = studio - (studio * 0.2)
print(f"Apartment: {apartment:.2f} lv.")
print(f"Studio: {studio:.2f} lv.")
