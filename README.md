# PW-lib
Pure Widgets

A little library made to simplify making GUIs for small projects that use screens by providing a set of widgets to help with pixel management.

Inspired by GTK, this library proposes a fundamental concept of `Widget`, from which are derived other classes.
It is a Work in (little so far) Progress, made for little microcontroller projects that use a screen (more specifically, made for [my tamagotchi project](https://github.com/AKArien0/multi-tamagotchi)). It provides a skeletton structure that can be used on any display.

## Widgets

* If a widget's role is not to actually display something, their implementation is complete. They usually handle other widgets or theoratical concepts.
* Displayers are incomplete : they lack an implementation for their `display()` and `hide()` methods. These implementations are to be added by you for the Displayer widgets you want to use, in order to be used with any specific library your model of screen might require.
  To define a `.display()` and `.hide()`, define the method as you would any other, for example :
```cpp
namespace PW{
  void Image::display(){
    // call your displaying function
  }

  void Image::hide(){
    // call your hiding function
  }

}

void PW::TextBox::display(){
  // or whatever you fancy !
}
```

Further documentation in the [github wiki](https://github.com/AKArien0/PW-lib/wiki).
