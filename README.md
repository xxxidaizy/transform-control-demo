实现一个Three.js拖拽旋转控制器
这个变换控制器允许用户通过鼠标或触摸来旋转、平移和缩放3D对象。
实现原理
导入Three.js模块：代码首先从Three.js库中导入了多个几何体、材质、对象等模块，用于创建和控制3D对象。

定义辅助变量和常量：定义了一些辅助变量和常量，如_raycaster用于光线投射，_tempVector等用于临时存储计算结果。

TransformControls类：这是主要的控制器类，继承自Three.js的Object3D类。它包含了平移、旋转和缩放的功能，并且可以处理鼠标和触摸事件。

TransformControlsGizmo类：这个类定义了变换控制器中的各种操作手柄（如旋转、平移、缩放手柄），以及它们的几何形状和材质。

TransformControlsPlane类：这个类定义了一个平面，用于与用户交互，例如在平移模式下，用户可以通过拖动平面来移动对象。

用途
这个变换控制器可以用于3D建模、游戏开发、虚拟现实等场景中，允许用户通过直观的交互方式来操作3D对象，而不需要编写复杂的代码。

注意事项
依赖Three.js：这段代码依赖于Three.js库，因此需要在项目中引入Three.js才能正常运行。
性能考虑：由于变换控制器需要处理大量的几何计算和渲染，可能会对性能产生影响，特别是在处理复杂场景时。
事件处理：代码中定义了多个事件处理函数，如pointerHover、pointerDown、pointerMove和pointerUp，这些函数用于处理鼠标和触摸事件，实现用户交互。
自定义属性：TransformControls类通过defineProperty函数定义了一些自定义属性，如camera、object、enabled等，这些属性可以通过getter和setter方法进行访问和修改，并且会触发相应的事件。