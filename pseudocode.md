# INIT: Making the variables for my program
1. Bathroom 
    * Room where hands are washed

    **PROPERTIES:**
    - location
2. Sink
    * The place where you hands are washed
    * Where water is released and drained

    **PROPERTIES:**
    - containsWater
3. Knobs/Handles
    * Used to make water come out

    **PROPERTIES:**
    - waterFlow
    - waterTemp
4. Soap
    * Used to get rid of germs
    * Makes hands clean

    **PROPERTIES:**
    - despenseSoap
    - suds
5. Hand Towel
    * Makes hands dry

    **PROPERTIES:**
    - dry
6. Hands
    * What need to become clean
    * Used to turn water on and off
    * Need to use soap and hand towel

    **PROPERTIES:**
    - turn
    - cleanliness 

# Functionality:
## PREP:
``` 
FUNCTION findSink:
    FOR {
        IF not looking at sink {
            turn 10 degrees until looking at sink
        }
        ELSE {
            END
        }
    }

FUNCTION findSoap:
    IF soap is not on counter{
        look under sink
    }
    ELSE IF {
        go to kitchen/other bathroom and bring back to bathroom you were in
    }
    ELSE {
        END
    }

FUNCTION findTowel:
    IF handTowel is not on counter/hanger {
        go get a towel and bring it back to the bathroom
    }
    ELSE {
        END
    }