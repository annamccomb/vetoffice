# vetoffice
exercise 02B

Pet-and-owner-and-service(PetName, PetType, PetBreed, PetDOB, OwnerLastName, OwnerFirstName, OwnerPhone, OwnerEmail, Service, Date, Charge)

# Dependencies:
PetName-->(PetType, PetBreed, PetDOB)
OwnerEmail--->(OwnerLastName, OwnerFirstName, OwnerPhone)
OwnerPhone--->(OwnerLastName, OwnerFirstName, OwnerEmail)
Service--->(Date, Charge)

Right now, the candidate key for the pet-and-owner-and-service table is PetName. Not all determinants are candidate keys.

# Break into 3 relations: Pet and Owner and Service
Pet(PetName, PetType, PetBreed, PetDOB, ForeignKey)
Owner(OwnerLastName, OwnerFirstName, OwnerPhone, OwnerEmail)
Service(Date, Charge, ForeignKey)

Owner Relation:
OwnerEmail--->(OwnerLastName, OwnerFirstName, OwnerPhone)
OwnerPhone--->(OwnerLastName, OwnerFirstName, OwnerEmail)

# Candidate keys for owner: OwnerEmail, OwnerPhone
Now, both determinants are candidate keys.

Pet Relation:
PetName-->(PetType, PetBreed, PetDOB)

The determinant for Pet is a candidate key: PetName.

Service Relation:
Service--->(Date, Charge)

The determinant for Service is a candidate key: Service.

# We will choose OwnerPhone as the primary key. 

Owner(OwnerPhone, OwnerLastName, OwnerFirstName, OwnerEmail)
Pet(PetName, PetType, PetBreed, PetDOB, OwnerPhone)
Service(Date, Charge, PetName)

