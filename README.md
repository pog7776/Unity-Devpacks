# My Devpacks of all time

## Index

| Name       | Namespace                                   | Git URL                                                                                                    |
|------------|---------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Dev Art    | com.jack.unity.packages.devpacks.art.devart | https://github.com/pog7776/Unity-Devpacks.git?path=/Art/DevArt/com.jack.unity.packages.devpacks.art.devart |
| Attributes | com.jack.unity.packages.devpacks.attributes | https://github.com/pog7776/Unity-Devpacks.git?path=/Attributes/com.jack.unity.packages.devpacks.attributes |
| Drone      | com.jack.unity.packages.devpacks.drone      | https://github.com/pog7776/Unity-Devpacks.git?path=/Drone/com.jack.unity.packages.devpacks.drone           |
| Physics    | com.jack.unity.packages.devpacks.physics    | https://github.com/pog7776/Unity-Devpacks.git?path=/Physics/com.jack.unity.packages.devpacks.physics       |
| Vehicles   | com.jack.unity.packages.devpacks.vehicles   | https://github.com/pog7776/Unity-Devpacks.git?path=/Vehicles/com.jack.unity.packages.devpacks.vehicles     |

## Usage

Unity seems to be a bit uncooperative with Github packages.

### Example `manifest.json`
```
{
    "dependencies": {
        "com.jack.unity.packages.devpacks.art.devart": "https://github.com/pog7776/Unity-Devpacks.git?path=/Art/DevArt/com.jack.unity.packages.devpacks.art.devart",
        "com.jack.unity.packages.devpacks.attributes": "https://github.com/pog7776/Unity-Devpacks.git?path=/Attributes/com.jack.unity.packages.devpacks.attributes",
        "com.jack.unity.packages.devpacks.drone": "https://github.com/pog7776/Unity-Devpacks.git?path=/Drone/com.jack.unity.packages.devpacks.drone",
        "com.jack.unity.packages.devpacks.physics": "https://github.com/pog7776/Unity-Devpacks.git?path=/Physics/com.jack.unity.packages.devpacks.physics",
        "com.jack.unity.packages.devpacks.vehicles": "https://github.com/pog7776/Unity-Devpacks.git?path=/Vehicles/com.jack.unity.packages.devpacks.vehicles",
    }

    "scopedRegistries": [
        {
            "name": "Github Packages",
            "url": "https://npm.pkg.github.com/@pog7776/",
            "scopes": [
                "com.jack.unity.packages.devpacks"
            ]
        }
    ]
}
```

**Note**

`scopedRegistries` doesn't really seem to work for github.

- https://discussions.unity.com/t/using-github-packages-registry-with-unity-package-manager/784073
- https://discussions.unity.com/t/npm-registry-authentication/778442
- https://docs.unity3d.com/6000.1/Documentation/Manual/upm-scoped-host.html
- https://docs.unity3d.com/6000.1/Documentation/Manual/cus-share.html
- https://docs.unity3d.com/6000.1/Documentation/Manual/upm-git.html

Using "@" notation in url to force it as Unity does not support "@" notation in the scope. 