# navXLibrary
Team 4904's navX submodule.

## Purpose
This submodule is meant to be used within another repository to enable the parent repository to use the navX library.

## Use instructions
This repository should be cloned into the `~/wpilib/user/java/lib` folder. To do this, run the following command:
```
git clone git@github.com:RoboticsTeam4904/4904-USERLIBS.git ~/wpilib/user/java/lib
```

Once it's there, add the following to your repository's  `.classpath` file:

```
<classpathentry kind="var" path="USERLIBS_DIR/navx_frc.jar" sourcepath="USERLIBS_DIR/navx_frc-sources.jar"/>
<classpathentry kind="var" path="USERLIBS_DIR/CTRLib.jar"/>
```

Make sure that your `build.properties` has no `userLibs` line. If there is one, comment it out.

## NavX Update instructions
This submodule should be updated whenever Kauai Labs, Inc. releases a new compiled `navx_frc.jar` file. When that happens:

1. Overwrite this repo's `navx_frc.jar` with the updated version.
2. Run `sh generate-sources.sh` to automatically regenerate the `navx_frc-sources.jar` file.
3. Branch, commit, test, pull request, get it merged
4. Pull the changes to your local clone of the repository
