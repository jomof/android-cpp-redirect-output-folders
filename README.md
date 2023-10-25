This example demonstrates redirecting the CMake-generated build directory to another location.

To do this, you can create a file called CMakeSettings.json:

```
{
  "configurations": [{
    "name": "android-gradle-plugin-predetermined-name",
    "inheritEnvironments": ["ndk"],
    "buildRoot": "${ndk.moduleBuildRoot}/${ndk.variantName}/${ndk.abi}"
  }]
}
```

The configuration name "android-gradle-plugin-predetermined-name" is important and special to Android Gradle Plugin. CMakeSettings.json settings under this name are applied to the generated CMake project.

Once this is done, you can do Build->Refresh Linked C++ Projects to see the generated CMake projects in their new location defined by "buildRoot" in CMakeSettings.json.



