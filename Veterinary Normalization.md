# Normalization Process

## 1. Identify all the candidate keys of the relation
   * Pet Name
## 2. Identify all the functional dependencies in the relation
   * Pet Name &#8594; (PetType, PetBreed, PetDOB, _PetName_)
   * OwnerLastName &#8594; (OwnerFirstName, OwnerPhone, OwnerEmail, _OwnerLastName_)
   * Service &#8594; (Charge, Date, _Service_)
## 3. Examine the determinants of the functional dependencies. If any determinant is not a candidate key, relation is malformed
   * The relation is malformed because some of the determinants are not candidate keys.
      * Service
      * OwnerLastName
## 4. Repeat step 3 until every determinant of every relation is candidate key.
   * After creating new relations for the functional dependencies;
      * Pet(**PetName**, PetBreed, PetDOB)
      * Owner(**OwnerLastName**, OwnerFirstName, OwnerPhone, OwnerEmail) 
      * Service(**Service**, Charge, Date)
