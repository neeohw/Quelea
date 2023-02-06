# Running Quelea on AARCH64 (ARM 64)

## Install Liberica Java 17
Head over to the [Downloads](https://bell-sw.com/pages/downloads/#downloads) section of Liberica Java and download Liberica Java SDK 17. Be sure to select the ARM Full JDK flavor!! (By default the x86 Standard JDK is selected. The Standard JDK doesn't have JavaFX)

## Compile Quelea
`cd Quelea; ./gradlew clean jar copyToDist`

## Run Quelea
`cd dist; java --add-exports=javafx.graphics/com.sun.javafx.css=ALL-UNNAMED --add-exports=javafx.base/com.sun.javafx.runtime=ALL-UNNAMED --add-exports=javafx.base/com.sun.javafx.event=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.scene.traversal=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.scene=ALL-UNNAMED --add-opens java.base/java.lang=ALL-UNNAMED --add-opens javafx.controls/javafx.scene.control=ALL-UNNAMED -Djdk.gtk.verbose=true -Djdk.gtk.version=2 -DVLCJ_INITX=no -Dfile.encoding=UTF-8 -Dprism.dirtyopts=false -Djavafx.cachedir=/tmp -jar Quelea.jar`
