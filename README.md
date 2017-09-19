# JPSpringMenu
SpringMenu is a sliding menu, similar to AndroidResidemenu, SlidingMenu,
The biggest difference between SpringMenu and other menus is that it gives flexibility bouncing, 
and this project combines the powerful animation elastic library called 
[Rebound](https://github.com/facebook/rebound) provided by Facebook<Br>
### [中文文档](https://github.com/peng8350/JPSpringMenu/blob/master/README_CH.md)

### Design Sketch
![SpringMenu](https://github.com/peng8350/JPSpringMenu/blob/master/art/main.gif)
<br>
### Usage
1.Gradle 
```
dependencies {
    compile 'com.jpeng.jpspringmenu:$latestVersion'
}
```
2.in Activity init
```
    // R.layout.view_menu is your custom menu Layout resourceId
    SpringMenu menu = new SpringMenu(this,R.layout.view_menu);
    
    // do something config for menu...
```
3. Don't forget to Rewrite dispatchTouchEvent in Activity
```
    @Override
    public boolean dispatchTouchEvent(MotionEvent ev) {
         return menu.dispatchTouchEvent(ev);
    }
```

### Thanks
[AndroidResideMenu](https://github.com/SpecialCyCi/AndroidResideMenu)

### License
```
MIT License

Copyright (c) 2017 Mr.peng

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```