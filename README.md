[![](https://jitpack.io/v/ngoconglinh/aGauge.svg)](https://jitpack.io/#ngoconglinh/aGauge)

CustomGauge
===========

## Quick Start

**aGauge** is available on jitpack.

Add dependency:

```groovy
implementation "com.github.ngoconglinh:aGauge:last-release"

```

## Usage

to use **aGauge**:

in **Setting.gradle**
```groovy
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        mavenCentral()
        maven { url 'https://jitpack.io' }
    }
}
```
### Attributes

Available view attributes:

* startAngel (left start angel in degrees) - please be informed that gauge is drawn as an arc from startAngel (where to start) with sweepAngel (how many degrees arc is); what is more it's clockwise (right - 0, bottom - 90, left - 180, top - 270 degrees); if for example you want full circle start on 90 with 360 sweepAngel
* sweepAngel - as described above
* startValue - scale start value
* endValue - scale end value
* strokeWidth - stroke width
* strokeColor - resource color (cannot be selector)
* strokeCap - style of circle stroke (BUTT - straight, ROUND - rounded)
* pointSize - defined for pointer drawn on current value (first example) - tells how wide pointer should be; if not set pointer is drawn from start value to current value (like second example)
* pointStartColor - used for gradient pointer (second example)
* pointEndColor - used for gradient pointer (second example)
* dividerSize - size of divider related to values; if declared dividers will be drawn(!); e.g. if your start value is 50 and end value is 120 dividerSize set to 2 means that divider will have 1/35 of gauge total width - in other words it will have size of 2 points of gauge scale
* dividerStep - tells how often dividers will be drawn; it's in percentage values(!); e.g. if you want to have dividers drawn each 20% of scale just set it to 20 and you will have 6 dividers drawn (with first and last)
* dividerColor - color of divider
* dividerDrawFirst - whether to draw first divider or no
* dividerDrawLast - whether to draw last divider or no



```xml
    <com.ngoconglinh.agauge.CustomGauge
            android:id="@+id/gauge1"
            android:layout_width="200dp"
            android:layout_height="200dp"
            android:layout_centerHorizontal="true"
            android:layout_below="@+id/button"
            android:paddingBottom="20dp"
            android:paddingLeft="20dp"
            android:paddingRight="20dp"
            android:paddingTop="20dp"
            app:gaugePointStartColor="@color/md_red_500"
            app:gaugePointEndColor="@color/md_red_500"
            app:gaugePointSize="6"
            app:gaugeStartAngle="135"
            app:gaugeStrokeCap="ROUND"
            app:gaugeStrokeColor="@color/md_grey_400"
            app:gaugeStrokeWidth="10dp"
            app:gaugeStartValue="0"
            app:gaugeEndValue="1000"
            app:gaugeSweepAngle="270"/>

```
&nbsp;

***from*** [![](https://github.com/pkleczko/CustomGauge)]
