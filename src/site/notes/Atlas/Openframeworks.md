---
{"dg-publish":true,"permalink":"/atlas/openframeworks/","tags":["🌱","creative-coding","cpp","programming","openframeworks"],"updated":"2024-11-15T13:12:48.882-08:00"}
---


## Getting OpenFrameworks on Mac working with VS Code
Let's be honest, the documentation for OpenFrameworks leaves alot to be desired and has so much "implied knowledge" that isn't stated, so this is my attempt at documenting what it took for me to get OpenFrameworks working on my M3 Macbook.

### Project Generator
For whatever reason, on Mac, you have to move the ProjectGenerator.app file up one directory, and then back into the `projectGenerator` folder. Also, you can't open it from the command line, you **must** double click on it to make it show up.

### There are no `.code-workspace` files generated
Well this is annoying. The Project Generator assumes I'm using xcode. XCode is hot garbage, so I don't want to use it as my primary editor. I use VS Code (eventually Cursor) for my dev environment.

They do mention that the examples should have vs code project files, and luckily they are pretty simple, so we just need to update the relative paths.

```json
{
        "folders": [
                {
                        "path": "."
                },
                {
                        "path": "${workspaceRoot}/../../../../libs/openFrameworks"
                },
                {
                        "path": "${workspaceRoot}/../../../../addons"
                }
        ],
        "settings": {}
}
```

### But I don't have the tasks mentioned in the docs?
Unfortunately, that didn't work as expected. It loads fine, and now I can see all the project files, but the build task still doesn't exist, so I'm going to try opening one of the examples.

The examples are working correctly, so what's missing? `.vscode/tasks.json`, `.vscode/launch.json`, and `.vscode/c_cpp_properties.json`, so let's copy those over.

With that, I was able to build and run from VSCode

## The addons I always enable
- ofxGui
- ofxOsc

## 3rd party addons that I like to use


