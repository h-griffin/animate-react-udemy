# animating react apps
# Useful Resources & Links
- [More on CSS Transitions:](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions)
- [More on CSS Animations:](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations)
- [More on ReactTransitionGroup:](https://github.com/reactjs/react-transition-group)
- [Alternative => React Motion:](https://github.com/chenglou/react-motion)
- [Alternative => React Move:](https://github.com/react-tools/react-move)
- [Animating Route Animations:](https://github.com/maisano/react-router-transition)

## css transitions 
- inside class 
- default css will decide 

## css animations 
- set keyframes 
- animate property inside class

## react animations
- react does not wait for css animation to finish
- removing happens instantly 

- [react transition group github](https://github.com/reactjs/react-transition-group)

> $ npm install react-transition-group --save

- Transition component -set classes manually with .join(' ')
`<Transition in={this.state.showBlock} timeout={}>`
              ^                       ^
            show                  how long naimation is played

- timeout ( miliseconds )
    - time between 
    - entering > entered
    - exiting > exited

- return arrow function to show state

- div still takes up space when not displayed (style=exited)

- props to transition element
    - mount on enter
    - unmount on exit
- style
    - exiting will show animation
    - style = exiting

- **use these to run code at certain times /stack animations**
    - onEnter
    - onEntering
    - onEntered
    - onExit
    - onExiting
    - onExited

## CSSTransition

- cycles through calsses and merges them to element
- no not have to manually .join(' ') classes
- set animation classes in css file

- classnames='fade-slide'
    - fade-slide
    - fade-slide-enter              << removed after 1 fame (init class)
    - fade-slide-enter-active           < play animation
    - fade-slide-exit               << removed after 1 fame (init class)
    - fade-slide-exit-active            < play animation

```
    <CSSTransition 
        mountOnEnter
        unmountOnExit
        in={props.show} 
        timeout={animationTiming}
        classNames="fade-slide"           << 'trunk'
        >
```

### customize CSSTransition

```
classNames={{                   << obj /bypass all the classnames and use custom
    enter: '',
    enterActive: 'ModalOpen',
    exit: '',
    exitActive: 'ModalClosed'
    // appear: 
    // appearActive:
}}
```

## Transition Group
- use for dynamic lists

```
<TransitionGroup 
    component='ul'      << default is a div comp
    className='List'
    >
```

- **must be used with CSSTransition**


## [react move](https://github.com/sghall/react-move)
## [react motion](https://github.com/chenglou/react-motion)
- emulates real world physics
## [react router transition](https://github.com/maisano/react-router-transition)
- built off react motion

