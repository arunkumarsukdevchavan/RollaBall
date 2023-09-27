# RollaBall

## Aim:
To Roll a Ball using C# program in unity .
## Algorithm:

1. File -> Scene -> Select the scene -> Save as-> New folder(Scenes)-> File name (MiniGame)

2. Heirarchy -> 3D Object-> Plane 
[ Right side-> Inspector-> Change the name of plane (Name: Ground)
Transform -> Reset
Edit -> FrameSelected ]

3. Scale the ground by giving the scaling value as x=4 y=1 z=4

4. Heirarchy -> 3D Object-> Sphere
[ Right side-> Inspector-> Change the name of plane (Name: Player)
Transform -> Reset
Edit -> FrameSelected 
Transform -> Position -> y=0.5]

5. Hierarchy -> DirectionalLight
[ Inspector -> Change the color to white (255,255,255)]

6. Create a folder in project and name as Materials
[Material folder -> Create -> Material (Name: Background)
Inspector ->Surface Inputs ->BaseMAp (Choose the color) 
Metallic map-> 0
Smoothness -> 0.25
Drag the Background to the plane and release the mouse

Material folder -> Create -> Material (Name: Sphere)
Inspector ->Surface Inputs ->BaseMAp (Choose the color)
Metallic map-> 0
Smoothness -> 0.75
Drag the Sphere material to the ball and release the mouse

 7. Hierarchy -> Player-> Inspector ->Add component-> Rigidbody

8. Create a new script -> Create a folder in project (Name: Scripts)
Hierarchy -> Player -> Inspector-> AddComponent-> NewScripts-> PlayerController( Click create and Add)
Copy the PlayerController and drag to Script folder
Double click the PlayerController file and type the coding

## Program:
Name : ARUN KUMAR SUKDEV CHAVAN

Reg.no : 212222230013
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class balls : MonoBehaviour
{
    float XForce = 5.0f;
    float zForce = 20.0f;
    float yForce = 10.0f;
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        float x = 0.0f, y = 0.0f, z = 0.0f;
        if(Input.GetKey(KeyCode.A))
        {
            x = x - XForce;
        }
        if (Input.GetKey(KeyCode.D))
        {
            x = x + XForce;
        }
        if (Input.GetKey(KeyCode.W))
        {
            z = z - zForce;
        }
        if (Input.GetKey(KeyCode.S))
        {
            z = z + zForce;
        }
        if (Input.GetKey(KeyCode.Space))
        {
            y = yForce;
        }
        GetComponent<Rigidbody>().AddForce(x, y, z);
    }
}
```

## Output:
![output](https://user-images.githubusercontent.com/121222763/265992560-938795f6-d8df-44fc-883c-f576625cbe86.png)

## Result:
Thus, The 3D application for Roll the Ball objects in unity is developed successfully.
