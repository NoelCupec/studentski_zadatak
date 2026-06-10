## Section 2: Modern C++

# Task 1: Legacy Resource Wrapper (RAII)

Rješenje koristi RAII princip.

Konstruktor preuzima vlasništvo nad "resource file-om" putem funkcije fopen().

Destruktor automatski oslobađa taj "resource" pomoću fclose(), čime se osigurava sigurnost u slučaju iznimki i sprječavaju curenja "resource-a".

# Task 2: Asynchronous Worker Pool (Threading)


