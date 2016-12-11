# Usage

1. Add a Navmesh to your level.
  1. Check if there is already a Navmesh in existence by pressing **P**. If one exists, you will see a green overlay on your level. It should cover the entire area you wish your guard to be able to travel on. If one already exists, skip these steps and start with adding the guard to your level.
  1. If not, switch to the *Modes* panel (on the left-hand side of the window, by default) and either search for "Nav Mesh Bounds Volume" or choose it from the Volumes tab. Drag it into your level.
  1. Scale this volume to encompass the entire area you want the guard to be able to access. Again, press **P** to see a preview of the Navmesh.
  1. If you're having trouble, contact Jordan. In the future there will be a walkthrough of recasting Navmeshes and such, but for the sake of time and brevity these steps will break off here.
1. Drop the guard into your level where you'd like him to stand.
1. Under the "Nav Movement" category of the Details panel (about three quarters of the way down, or you can use the Details panel search bar and look for "nav"), change the "Preferred Nav Data" dropdown to "RecastNavMesh"
1. Test your guard by playing the game and running into the blinking sphere surrounding him. If there is a line of sight between him and your character, and you are within his trace volume, he should start chasing you.

# In the Future

Long-term, the guards' field of view will be updated to a more realistic trace and they will patrol along a preset path when not aggravated.