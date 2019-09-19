# Normalization Process

## 1. Identify all the candidate keys of the relation
   * Pet Name
## 2. Identify all the functional dependencies in the relation
   * Pet Name &#8594; (PetType, PetBreed, PetDOB, OwnerLastName, OwnerFirstName, OwnerPhone, OwnerEmail, Service, Date, Charge)
   * OwnerEmail &#8594; (OwnerLastName, OwnerFirstName, OwnerPhone)
   * OwnerPhone &#8594; (OwnerLastName, OwnerFirstName, OwnerEmail)
   * Service &#8594; (Charge, Date)
## 3. Examine the determinants of the functional dependencies. If any determinant is not a candidate key, relation is malformed
   * The relation is malformed because some of the determinants are not candidate keys.
## 4. Repeat step 3 until every determinant of every relation is candidate key.
   
