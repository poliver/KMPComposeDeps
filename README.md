# KMPComposeDeps
Minimum repro for https://github.com/autonomousapps/dependency-analysis-android-gradle-plugin/issues/907

Running `./gradlew buildhealth` yields the following output:
```
Advice for :app
Unused dependencies which should be removed:
  implementation 'androidx.compose.foundation:foundation-layout:1.5.0-beta02'
  implementation 'androidx.compose.foundation:foundation:1.5.0-beta02'
  implementation 'androidx.compose.material3:material3:1.2.0-alpha02'
  implementation 'androidx.compose.runtime:runtime:1.5.0-beta02'
  implementation 'androidx.compose.ui:ui-graphics:1.5.0-beta02'
  implementation 'androidx.compose.ui:ui-text:1.5.0-beta02'
  implementation 'androidx.compose.ui:ui-unit:1.5.0-beta02'
  implementation 'androidx.compose.ui:ui:1.5.0-beta02'

Transitively used dependencies that should be declared directly as indicated:
  implementation 'androidx.compose.foundation:foundation-android:1.5.0-beta02'
  implementation 'androidx.compose.foundation:foundation-layout-android:1.5.0-beta02'
  implementation 'androidx.compose.material3:material3-android:1.2.0-alpha02'
  implementation 'androidx.compose.runtime:runtime-android:1.5.0-beta02'
  implementation 'androidx.compose.ui:ui-android:1.5.0-beta02'
  implementation 'androidx.compose.ui:ui-graphics-android:1.5.0-beta02'
  implementation 'androidx.compose.ui:ui-text-android:1.5.0-beta02'
  implementation 'androidx.compose.ui:ui-unit-android:1.5.0-beta02'
```
