# Navigation System
Add one of these states to a canvas created to display a minimap for your game and add the other state to a orthographic camera that displays your game's full map. The first state will allow you to see a zoomed-in minimap, it will allow you to open the full zoomed-out minimap by pressing a key and be able to zoom in your character's position. The second state will allow the camera to follow the character when zooming in or out. 

## Contents

This component is made from the following behaviours:
- `Following`
- ` Vision`

And the following states:
- `CamFollow`
- `Map`

### CamFollow

When added to the orthographic camera that displays the full zoomed-out map, this state will allow the mentioned camera to follow the player through the map when zooming in or out. In order for this to work, the character controller will need to be dragged into the inspector so it is taken as a target.

### Map

When added to a canvas made specially for your minimap, this state will display a zoomed-in camera that will follow your player around your game. It will also allow you to open a full zoomed-out version of the previous view and finally it will let you zoom in your character's position as well as zooming-out. This view will desactivate or activate depending on the times the key is pressed. For this to work, you will need two render textures, one showing the whole map of your game and one showing your character's minimap. A minimap camera and a full map camera are also needed. When this is done, add a canvas to your scene and attach as children both of the render textures, adding the Map state, dragging both textures to their adequate places, adding the desired minimun and maximun zoom, the zoomed out camera and the speed we would like. This will give you a small minimap that can be opened by pressing a key, making it full. 
