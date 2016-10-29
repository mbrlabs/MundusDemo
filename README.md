# MundusDemo
A libGDX demo project showcasing the [Mundus world editor](https://github.com/mbrlabs/Mundus) and the libgdx runtime

## Building the gdx-runtime
The gdx-runtime of Mundus is not finished yet, thus i have not yet published it to maven central. So in order
to build this project you need to compile the runtime from source. You can find the Mundus editor and the runtime
in this repository: [https://github.com/mbrlabs/Mundus](https://github.com/mbrlabs/Mundus)

You need to build 2 jars and place them in the corresponding folder of the MundusDemo project:
- `./gradlew gdx-runtime:distRuntime` compiles the Mundus runtime and copies the generated jar to `gdx-runtime/build/libs/mundus-gdx-runtime-0.1.0.jar`
- `./gradlew gdx-runtime:distRuntimeSources` collects the source files and bundles them in a jar located at `gdx-runtime/build/libs/mundus-gdx-runtime-0.1.0-sources.jar`

`mundus-gdx-runtime-0.1.0.jar` must be placed in `core/libs` of this repository.
`mundus-gdx-runtime-0.1.0-sources.jar` must be placed in `html/libs` of this repository.

The sources jar is only required for the GWT build.
To speed up the process of compiling the runtime and coping it to this project it's recommended to write a little shell script.

## Building MundusDemo
Once you compiled the runtime and placed the jars in the correct folders, you can run the project as usual.

## Mundus project
The mundus project is included in this project (folder DemoProject). You can import it with the Mundus editor.
You have to set the export folder to YourPathToThisProject/android/assets/mundus