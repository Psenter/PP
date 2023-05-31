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
```
## Washing:
```
FUNCTION turnOnWater:
    a. Put left hand on left knob/handle
    b. Turn knob 30 degrees so water starts flowing
    c. REPEAT steps a and b but with right hand and right knob/handle

FUNCTION waterTempurature:
    a. Stick hand in water to see if it is to hot or to cold
    b. FOR {
        IF waterHot {
            Put left hand on left knob and turn 5 degrees to the left
        }
        ELSE IF waterCold {
            Put right hand on right knob and turn 5 degrees to the right
        }
        ELSE {
            Water tempurature feels right END
        }
    }

FUNCTION soapyHands:
    a. Put hands into water for 1 second then take them out
    b. Put right hand under soap dispenser spout
    c. Put left hand on top of soap dispenser and push down
    d. Cup hands and put them together
    e. Rub in a circular motion for 5 seconds 

FUNCTION wash:
    a. Put hands into water
    b. Rub hands in circular motion for 30 seconds in water
    c. Put left palm towards ceiling
    d. Gently rub right hand finger nails  back and forth on left palm
    e. REPEAT step c and d, but switch hand placement
```
## Turn off water:
```
FUNCTION waterOff:
    a. Take hands out of water
    b. Place left hand on left knob and turn to the left
    c. REPEAT step b with right hand and knob and turn to the right
```
## Drying:
```
FUNCTION dryHands:
    a. Pick up hand towel
    b. Put towel inbetween hands
    c. Rub hands in a circular motion for 5 seconds
        IF hands still wet {
            REPEAT step c
        }
        ELSE {
            END
        }
```