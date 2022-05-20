# Unicorn Pegasus

Rigged glTF vehicle that an avatar can sit on and commandeer.

![image](https://user-images.githubusercontent.com/64185677/169426852-f9b87bf8-9fe6-4639-b7d5-806b2ace9c11.png)

## Creating Vehicles:

Bring your custom vehicle to life in Webaverse and ride around in style. 

## Hosted Webaverse Environments:

To get started with a customized vehicle, follow these simple steps.

1. Go to the GitHub “hovercraft” example repo: [https://github.com/webaverse/hovercraft](https://github.com/webaverse/hovercraft) and fork it to your personal account.

![image](https://user-images.githubusercontent.com/64185677/169426128-2c0b9f90-e523-4c95-baa7-42e93481c68b.png)

2. Add your own .glb model into the repo —- Or just use the existing model that’s already there. 

3. Next, open the .metaversefile and edit it.

![image](https://user-images.githubusercontent.com/64185677/169426188-ed345816-c391-4e9f-9152-2bd08201fe70.png)

4. Search the file for “.glb” ****and update the reference ******from “****.glb***” to the name of the model you want to use (i.e., ***“mymodel.glb”* ).  ****Then save and commit the changes. For more information about .metaversefile, look [here](https://www.notion.so/metaversefile-628e2c46f49345dfa68a2eab7b89d3f5).

![image](https://user-images.githubusercontent.com/64185677/169426248-216b006a-4b84-4009-aaf2-80a572240752.png)

5. Your model is now ready to be used in any Webaverse scene! There’s just one last step required in order to reference it from a hosted Webaverse installation: enable the GitHub Page on your repo. Head over to the settings for the repo, go to the Pages section, set the branch as master and save it. Finally, make a note of the GitHub page URL for later.

[Video Tutorial](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/56559169-2d43-4ea5-ab48-55123eb148ef/bandicam_2022-02-19_22-29-09-026.mp4)

1. You can use any of our template scenes or make your own. To add a model in a template scene, go the **“app/scenes”** folder in your cloned Webaverse app and open any of the .scn files.
2. Copy and paste this into the .scn file right before the closing “]” bracket.

```json
,{
	"position": [
		0,
		1,
		0
	],
	"quaternion": [
		0,
		0,
		0,
		1
	],
	"start_url": "https://webaverse.github.io/hovercraft/"
}
```

1. Set “start_url” to the url of the GitHub Page for your repository. You can also adjust the starting position and rotation of the model based on where you want it in your scene. Now save the file and you’re good to go. 
2. Go to [https://app.webaverse.com](https://app.webaverse.com) or some other hosted version of the app, drag your .scn file into the browser and experience your model brought to life.

## Local Webaverse Environments:

1. Go to the GitHub repo: [https://github.com/webaverse/hovercraft](https://github.com/webaverse/hovercraft) and download the repo as **a zip.**
2. Extract the zip folder into your already available Webaverse **“app”** folder.
3. Add your own .glb model into the extracted folder —- Or just the existing model that’s already there. 
4. Your model is now ready to be used in any Webaverse scene! You can use any of our template scenes or make your own. To add a model in a template scene, go the **“app/scenes”** folder in your cloned Webaverse app and open any of the .scn files.
5. Copy and paste this into the .scn file right before the closing “]” bracket.

```json
,{
	"position": [
		0,
		0,
		0
	],
	"quaternion": [
		0,
		0,
		0,
		1
	],
	"start_url": "/hovercraft-master/"
}
```

1. You can also adjust the starting position and rotation of the model based on where you want it in your scene. Now save the file and you’re good to go. Run the app, enter the edited scene and enjoy!

Checkout our [walkthrough video](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/44ec83df-ccc0-4a92-b06d-1c088bd39e46/bandicam_2022-02-26_19-26-15-142.mp4) on how to create a vehicle.

## `.metaversefile`

The .metaversefile goes in the directory with the GLB file in order to create the XRpackage.

```
{
  "name": "unicornpegasus",
  "start_url": "unicornpegasus.glb",
  "components": [
    {
      "key": "sit",
      "value": {
        "subtype": "saddle",
        "sitOffset": [0, 0.6, 0],
        "walkAnimation": ["wing_2_low|Take 001|BaseLayer", "wing_2_low001|Take 001|BaseLayer", "Object001|Take 001|BaseLayer", "Object002|Take 001|BaseLayer", "Object003|Take 001|BaseLayer", "Object004|Take 001|BaseLayer"],
        "walkAnimationHoldTime": 1,
        "walkAnimationSpeedFactor": 0.1,
        "speed": 0.02,
        "damping": 0.99
      }
    }
  ]
}
```
