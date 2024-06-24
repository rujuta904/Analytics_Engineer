Document: Hotel Chain Reservation System Schema - Key Relationships and Assumptions

Membership System:

The MembershipTypes table defines different tiers of membership (e.g., Silver, Gold, Platinum).
Each tier has a discount percentage and associated points.
MembershipActivities tracks a guest's membership history, including tier changes and point transactions.
Assumption: Guests can earn points through bookings and redeem them for discounts or perks.

Add-Ons:

AddOns table stores various additional services or items guests can purchase.
BookingsAddOns links specific add-ons to bookings, allowing multiple add-ons per booking.
Assumption: Add-ons are priced separately from room rates and can be quantified (e.g., extra towels, spa services).

Promotions:

The promotions table stores various offers or discounts.
BookingPromotions links promotions to specific bookings.
Assumption: Multiple promotions can be applied to a single booking, and they can be percentage-based or fixed-amount discounts.

Room Types and Rooms:

RoomTypes defines categories of rooms available in each hotel (e.g., Standard, Deluxe, Suite).
Rooms represent individual rooms, linked to a specific RoomType and Hotel.
Assumption: Room rates are associated with RoomTypes, allowing for dynamic pricing based on room category.

Hotels and Chains:

Hotels belong to Chains, representing the global hotel chain structure.
Assumption: Each hotel can have its own set of room types, amenities, and potentially localized promotions.

Bookings:

Central to the system, linking Guests, Rooms, and Hotels.
Connected to Payments, Reviews, and various other elements like add-ons and promotions.
Assumption: A booking is for multiple rooms and can accommodate multiple guests (adults and children).

Amenities:

Amenities can be associated with both Hotels and RoomTypes, allowing for both hotel-wide and room-specific features.

Images:

The Images table, along with junction tables (e.g., HotelImages, RoomImages), allows for multiple images to be associated with various entities in the system.

Key Assumptions:

- The system supports multi-currency operations (LocalCurrency in Hotels table).
- Guests can accumulate points through bookings, which are tracked in MembershipActivities.
- The system allows for flexible pricing with room types, add-ons, and promotions all factoring into the total price.
- Reviews are tied to specific bookings, ensuring verified guest feedback.
- The schema supports a hierarchical structure (Chain > Hotel > Room Type > Room) for better management and scalability.
