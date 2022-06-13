# EntityCulling-WithoutFabricApi
A script for building https://github.com/tr7zw/EntityCulling without Fabric API
```
git clone --branch 1.19 https://github.com/tr7zw/EntityCulling && \
cd EntityCulling && \
sudo chmod +x gradlecw && \
a=EntityCulling-Fabric/src/main && \
b=$a/java/dev/tr7zw/entityculling/EntityCullingMod.java && \
c=$a/resources/fabric.mod.json && \
sed -i /fabric.api/d $b && \
sed -i /KeyBindingHelper/d $b && \
sed -i /START_WORLD_TICK/,+2d $b && \
sed -i /START_CLIENT_TICK/,+3d $b && \
sed -i '/"fabric": "*"/d' $c && \
./gradlecw build && \
mv EntityCulling-Fabric/build/libs/*1.19.jar ..
```
