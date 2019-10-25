Useful Info For SASS
======
  
Index  
[Functions](#Functions)


Functions
------  
  
#### Function for Media Queries  
  
```
@mixin respond($breakpoint)
{
  @if $breakpoint == phone{
    @media (max-width: 37.5em) { @content};    
  }
  @if $breakpoint == tab-port{
    @media (max-width: 56.25em) { @content};
  }
  @if $breakpoint == tab-land{
    @media (max-width: 75em) { @content};
  }
  @if $breakpoint == big-desktop{
    @media (min-width: 112.5em) { @content};
  }
}
```  
  
  
  
[Index](#Index)
