## Section 2: Modern C++

# Task 1: Legacy Resource Wrapper (RAII)

The solution uses the RAII principle.

The constructor acquires ownership of a FILE*
resource through fopen().

The destructor automatically releases the resource
using fclose(), guaranteeing exception safety and
preventing resource leaks.
