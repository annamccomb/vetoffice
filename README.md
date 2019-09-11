# vetoffice
exercise 02B

Pet-and-owner(PetName, PetType, PetBreed, PetDOB, OwnerLastName, OwnerFirstName, OwnerPhone, OwnerEmail)

Dependencies:
PetName-->(PetType, PetBreed, PetDOB)
OwnerEmail--->(OwnerLastName, OwnerFirstName, OwnerPhone)
OwnerPhone--->(OwnerLastName, OwnerFirstName, OwnerEmail)

Right now, the candidate key for the pet-and-owner table is PetName. Not all determinants are candidate keys.

Break into 2 relations: Pet and Owner
Pet(PetName, PetType, PetBreed, PetDOB, ForeignKey)
Owner(OwnerLastName, OwnerFirstName, OwnerPhone, OwnerEmail)

Owner Relation:
OwnerEmail--->(OwnerLastName, OwnerFirstName, OwnerPhone)
OwnerPhone--->(OwnerLastName, OwnerFirstName, OwnerEmail)

Candidate keys for owner: OwnerEmail, OwnerPhone
Now, both determinants are candidate keys.

Pet Relation:
PetName-->(PetType, PetBreed, PetDOB)

The determinant for Pet is a candidate key: PetName.

We will choose OwnerPhone as the primary key. 

Owner(OwnerPhone, OwnerLastName, OwnerFirstName, OwnerEmail)
Pet(PetName, PetType, PetBreed, PetDOB, OwnerPhone)


