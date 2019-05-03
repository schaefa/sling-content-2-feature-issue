# Sling Content Package to Feature Model Issue

This demo project shows the drop of the embedded bundle
when converted with the **Sling Content Package to Feature
Model converter**.

## Setup

This project was created using the latest Sling Project
Archetype (1.0.1-SNAPSHOT) with the bundle embedded and
example merge option.

Then it was built and deployed onto Sling to verify that
both the package and bundle is deployed successfully.

## Conversion

The latest code of the converted was built from source
installed here (bin/ and lib/ folder are copied into this
project). The it was converted with:
```
./bin/cp2sf \
    -X \
    -b 20 \
    -c ui.apps/target/ui.apps-1.0.0-SNAPSHOT.zip \
    -a fm.artifact.out/ \
    -o fm.out/
```

## Result

The package is successfully converted and the embedded
bundle was removed from the package inside the
**ui.apps-1.0.0-SNAPSHOT-cp2fm-converted.zip** file
but the **ui.apps.json** file does not declare that
bundle **core-1.0.0-SNAPSHOT.jar**. 