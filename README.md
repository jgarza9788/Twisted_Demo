Twisted
-------------------------------------
[Asset Store Link](http://u3d.as/TMQ)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

Contact  
-------------------------------------
Questions, suggestions, help needed?  
Contact me at:  
Email: jgarza9788@gmail.com  
Cell: 1-818-251-0647  
Contact Info: [justingarza.net/contact](http://justingarza.net/contact/)
  
Description/Features
-------------------------------------
Awesome Twisted Effect! * Unity Free friendly.
* Fully commented C# code.
* Awesome demos!
Terms of Use
-------------------------------------
You are free to add this asset to any game you’d like
However:  
please put my name in the credits, or in the special thanks section. :)  
please do not re-distribute.  

Table of Contents 
-------------------------------------
1. Scripts
	* TwistedChangeCulling.cs
	* DemoScript1.cs
	* Other Scripts 
2. Shader(s)
	* Twisted(WorldSpace).Shader
3. Demo1
4. Demo2
5. How to Use
6. Known Issues


Scripts
-------------------------------------
**TwistedChangeCulling.cs**  
Allows you to change the Culling Option on material at Start.  
To find out more about culling [click here](https://docs.unity3d.com/Manual/SL-CullAndDepth.html).

**DemoScript1.cs**
Script used in Demo1 to change the settings based on sliders.

**DestoryPorthole.cs**  
Holds a method to destory the Porthole when done animating. (Used in Demo2)

**GeneratePorthole.cs.cs**  
Allows the projectile to create a portal on collision. (Used in Demo2)

####Other Scripts 
Just other scripts that are in this asset, they most used to make the demo work.

* AlwaysFace.cs  
* DestroyAfter.cs  
* OpenURLButton.cs  
* Rotate.cs  
* ShootOnClick.cs  
* SwitchScenes.cs  


Shader(s)
-------------------------------------
####Twisted(WorldSpace).Shader   
**Parameters**  

Radius:  
Radius of the Spiral in relation to the Quad it's on.  
Keep between 0 and 0.5.  

Angle:  
Angle of the Twist.  
Keep between -999 and 999. (optional)

Power:  
Changes the distance between each ripple.  
(this is not a good definition...please read code to see how it's used)

Cull:  
Controls what side(s) of the Quad will render.
 

Demo1 
-------------------------------------
This demo shows how the parameters of the shader effects how it looks, and how to change the parameters values using C#. See DemoScript1.cs for more info.

![Imgur](http://i.imgur.com/VkJTfu7.png)

~~~cs
		//update all the settings in the material
		
		TwistedMaterial.SetFloat("_Radius",RadiusSlider.value);
		RadiusText.text = "Radius: " + RadiusSlider.value.ToString("F2");

		TwistedMaterial.SetFloat("_Angle",AngleSlider.value);
		AngleText.text = "Angle: " + AngleSlider.value.ToString("F2");

		TwistedMaterial.SetFloat("_Power",PowerSlider.value);
		PowerText.text = "Power: " + PowerSlider.value.ToString("F2");

		RotateSpeedText.text = "RotateSpeed: " + RotateSpeedSlider.value.ToString("F2");
		RotateControlScript.speed = RotateSpeedSlider.value;
~~~

Demo2 
-------------------------------------
This demo displays how this Twisted effect can be used to make porthole like objects. 

![Imgur](http://i.imgur.com/TnEzXAM.png)

How to use
-------------------------------------
This is just a GameObject composed of a Quad,a few scripts, and a Shader; Therefore you can use it like a normal GameObject. (ie. drag it in a scene, or Instantiate) 

Please see Demos for example.
 
Known Issues 
-------------------------------------
While rendering one twisted effect on top of another the one on the bottom will not render correctly.

![Imgur](http://i.imgur.com/26lcfMc.png)



