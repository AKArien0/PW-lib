# PW-lib
Pure Widgets

A library made to simply bring OOP with any display.

Inspired by GTK, this library proposes a fundamental concept of `Widget`, from which are derived other classes.
It is a Work in Progress, made originally for arduino projects. It provides a skeletton structure that can be used on any display.

##Widgets

A widget can be either a Displayer or a Quiet. This distinction is purely theoretical and is a shorthand for wether a widget has a complete definition or not.

* Quiets are complete. They usually handle other widgets or theoratical concepts.
* Displayers are incomplete : they lack a definition for their `.display()` and `.hide()` method. These definitions are to be added by you for the Displayer widgets you want to use, in order to be used with any specific library of your choice.
  To define a `.display()` and `.hide()`, define the method as you normally would, for example :
```cpp
namespace PW{
  void Image::display(){
    // call your displaying function
  }

  void PW::display(){
    //call your hiding function
  }

}

void PW::TextBox::display(){
  // of course, this also works
}
```

Further documentation in the [github wiki](https://github.com/AKArien0/PW-lib/wiki).
