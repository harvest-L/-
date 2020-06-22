# 开发时遇到的兼容性问题汇总

1. ios下，从另外的页面返回，有可能会导致部分动画不执行，主要涉及的是transform动画
   解决方案： pageShow的时候，重新开启动画
            但是在ios的钉钉下，会发现这个部分动画还是不会执行。
            
2. ios下，开启3d，会引发层级错乱，也就是开启硬件加速的，，哪怕你最外面有个兄弟元素是fixed, z-index:9999都盖不住他。。
   解决方案：* 父亲元素overflow: hidden.
          
   参考方法：https://www.zhangxinxu.com/wordpress/2016/08/safari-3d-transform-z-index/
   
