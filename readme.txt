ConstraintLayout布局中，
一个控件可以基于其他控件，父控件、基准线（GuideLine）来约束自己的位置
约束布局的表达方式
layout_constraint[本源位置]_[目标位置]="目标ID"

1. 指定约束
对ConstraintLayout的属性设置，最重要的是理解属性所表达的含义，才能熟练使用。


2. 设置比例
在ConstraintLayout布局中，除了指定约束，还支持设置比例，类似于LinearLayout中的Bias项


3. 引导线约束
orientation="vertical" 表示引导线的方向竖直
layout_constraintGuide_begin="72dp" 表示距离页面

4. 控件填充
把宽高设置为0dp时，会根据位置自动填充

5. 控件宽高比
layout_constraintDimensionRatio 宽高比

高级内容
链式结构， 在ConstraintLayout约束布局中，还支持多个视图的排列组合，即链式结构。这与LinearLayout中多个控件排列的layout_weight属性非常类似，
通过设置不同的链式结构，就可以排列出不同的样式。
spread： 元素之间流有空隙，链的两侧也留有空隙，链的两侧也留有空隙，空隙的宽度相等。
spread inside： 元素之间留有空隙，链的两侧紧贴于容器两侧，控系的宽度相等。
weighted: 元素之间不含空隙，紧密排列
packed: 元素之间不含空隙，链的两侧留有空隙，且空隙宽度相等。
packed chain with bias： 元素之间没有空隙，而链的两侧

对于链式排列，需要元素与元素之间，首尾元素与容器之间的相互约束
对于weighted 有点类似linearlayout的weight属性，app:layout_constraintHorizontal_weight="1"