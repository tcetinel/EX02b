# Normalization Process

## 1. Identify all the candidate keys of the relation
   * Pet Name
## 2. Identify all the functional dependencies in the relation
   * Pet Name &#8594; (PetType, PetBreed, PetDOB, OwnerLastName, OwnerPhone, OwnerEmail)
   * OwnerPhone &#8594; (OwnerFirstName, OwnerPhone, OwnerEmail)
   * OwnerEmail &#8594; (OwnerFirstName, OwnerLastName, OwnerPhone)
   * Service &#8594; (Charge, Date)
  
## 3. Examine the determinants of the functional dependencies. If any determinant is not a candidate key, relation is malformed
   * The relation is malformed because some of the determinants are not candidate keys.
      * PetName is a candidate key
      * OwnerEmail is not a candidate key
      * OwnerPhone is not a candidate key
      * Service is not a candidate key
## 4. Repeat step 3 until every determinant of every relation is candidate key.
   * After creating new relations for the functional dependencies;
      * Pet(**PetName**, PetBreed, PetDOB, _OwnerEmail_)
      or
      * Pet(**PetName**, PetBreed, PetDOB, _OwnerPhone_)
      * Owner(**OwnerPhone**, OwnerFirstName, OwnerLastName, OwnerEmail) 
      or
      * Owner(OwnerPhone, OwnerFirstName, OwnerLastName, **OwnerEmail**)
      * Service(**Service**, Charge, Date)
