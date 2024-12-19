![image](https://github.com/user-attachments/assets/e4b3759f-da8f-4b14-aa3c-fcfa0535f8a0)














Rental Offer Controller
 1. GET /all-rental-offer/{rentalId}
 • Retrieves a list of all rental offers for a specific property, providing detailed information about each offer.
 2. GET /offer-id/{rentalOfferId}
 • Fetches detailed information about a specific rental offer by its ID.
 3. POST /accept-base-offer/individual-id/{individualId}/rental-id/{rentalId}
 • Allows a tenant to accept the base rental offer for a specific property.
 4. PUT /accept-or-reject-base/rental-id/{rentalId}/accepted/{accepted}
 • Enables the owner to accept or reject the base rental offer for a specific property.
 5. POST /start-offer/individual-id/{individualId}/rental-id/{rentalPropertyId}
 • Initiates a new negotiation offer from the tenant for a specific property.
 6. PUT /owner-offer/rental-offer-id/{rentalOfferId}
 • Allows the owner to respond to a rental offer with a new proposed rent.
 7. PUT /user-offer/rental-offer-id/{rentalOfferId}
 • Enables the tenant to respond to the owner’s proposed offer with a counteroffer.
- FranchiseRepository
- FranchiseContractRepository
8. PUT /individual-accept-reject/rental-offer-id/{rentalOfferId}
 • Allows the tenant to either accept or reject the owner’s proposed offer.
 9. PUT /owner-accept-reject/rental-offer-id/{rentalOfferId}
 • Enables the owner to either accept or reject the tenant’s final offer.
 10. GET /pending-by-owner/owner/{ownerId}
 • Retrieves a list of rental offers that are pending the owner’s response.
 11. GET /pending-by-individual/individual/{individualId}
 • Retrieves a list of rental offers that are pending the tenant’s response.
 12. GET /rental/{rentalPropertyId}/owner/{ownerId}/offers
 • Retrieves all offers for a specific rental property, ensuring the requesting user is the owner.

Rental Contract Controller
 1. POST /create-contract
 • Creates a new rental contract for a finalized offer.
 2. GET /rental-offer/{rentalOfferId}
 • Retrieves the rental contract associated with a specific rental offer.
 3. GET /individual/{individualId}/status/{status}
 • Fetches all contracts for a specific tenant, filtered by contract status (e.g., Active, Expired).
 4. GET /owner/{ownerId}/status/{status}
 • Fetches all contracts for a specific owner, filtered by contract status (e.g., Active, Expired).


Rental Property Controller
 1. GET /get-all
 • Retrieves a list of all rental properties.
 2. GET /get-rental-property/{id}
 • Fetches details of a specific rental property by its ID.
 3. POST /add/owner-id/{id}
 • Adds a new rental property for a specific owner.
 4. PUT /update/{id}
 • Updates details of an existing rental property.
 5. DELETE /delete/{id}
 • Deletes a specific rental property by its ID.
 6. GET /filter/city
 • Filters rental properties based on their city.
 7. GET /filter/location
 • Filters rental properties based on their specific location.
 8. GET /filter/unit-type
 • Filters rental properties based on their unit type (e.g., Shop, Office).

