#### 交易者公式

##### A B为代币，x y为代币数量



<center>交易后K值不变（无手续费）</center>

---

$$
\require{enclose}
\enclose{box}{
    \begin{array}{c}
    		\\
        交易前: \\
        x=1000 \\
        y=5000\\
        \\
        K=5000000\\
        \\
    \end{array}
}
\underrightarrow{\quad\bf用100个A购买B\quad}
\enclose{box}{
    \begin{array}{ccccccc}
    		\\
        交易后: \\
        x^1=1100 \\
        K=5000000\\
        \\
        y^1=K/x^1\approx4545.45\\
        \\

    \end{array}
}
\qquad\bf获得B数y_1为454.55(y-y^1)
$$



<center>交易后K值不变（0.3%手续费）</center>

---

$$
\require{enclose}
\enclose{box}{
    \begin{array}{c}
    		\\
        交易前: \\
        x=1000 \\
        y=5000\\
        \\
     	  \\
        K=5000000\\
        \\
        \\
    \end{array}
}
\underrightarrow{\quad\bf用10个A购买B\quad}
\enclose{box}{
    \begin{array}{ccccccc}
    		\\
        交易后: \\
        x^f=(1000+100*0.997) \\
        x^1=(1000+100) \\
        y^1=K/x^f\approx4546.69 \\
        \\

        K=50000\\
        K^1=x^1*y^1\approx5001359\\
        \\

    \end{array}
}
\qquad\bf获得B数y_1为453.31(y-y^1)
$$





#### LP公式

1. ##### 提供流动性

   <center>初始提供</center>

   ---

   $$
   \require{enclose}
   \enclose{box}{
       \begin{array}{c}
       		\\
           提供前: \\
           x=0 \\
           y=0\\
           \\
           L=0\\
           L_m=1000\\
           \\
       \end{array}
   }
   \underrightarrow{\quad\bf提供100个A和500个B的初始流动性\quad}
   \enclose{box}{
       \begin{array}{ccccccc}
       		\\
           提供后: \\
           x=1000 \\
           y=5000\\
           \\
   				\\
           L=\sqrt[2]{x*y}-Lm\\
           \\
   
       \end{array}
   }
   \qquad\bf获得初始流动性L=2236.07
   $$

   

   <center>中途提供</center>

   ---

   $$
   \require{enclose}
   \enclose{box}{
       \begin{array}{c}
       		\\
           提供前: \\
           x=1000 \\
           y=5000\\
           \\
           L=2236.07\\
           L_m=1000\\
           \\
       \end{array}
   }
   \underrightarrow{\quad\bf提供100个A和500个B的流动性\quad}
   \enclose{box}{
       \begin{array}{ccccccc}
       		\\
           提供后: \\
           x_1=100 \\
           y_1=500\\
   				\\
           L_{x1}=x_1*L/x\approx223.607\\
           L_{y1}=y_1*L/y\approx223.607\\
           L^1=L+min(L_{x1},L_{y1})=2459.677\\
   
           \\
           \\
   
       \end{array}
   }
   \qquad\bf获得L_1=L^1-L=223.607
   $$

2. 

2. #### 赎回流动性

<center>部分赎回</center>

---

$$
\require{enclose}
\enclose{box}{
    \begin{array}{c}
    		\\
        赎回前: \\
        x=1100 \\
        y=5500\\
        \\
        L=2459.677\\
        L_m=1000\\
        \\
    \end{array}
}
\underrightarrow{\quad\bf赎回223.607的流动性\quad}
\enclose{box}{
    \begin{array}{ccccccc}
    		\\
        赎回后: \\
        L_1=123.607 \\
				\\
        x_1=L_1*x/L\approx100 \\
        y_1=L_1*y/L\approx500\\
        x^{1}=x-x_1=1000\\
        y^{1}=y-y_1=5000\\
        L^1=L-L_1=2236.07\\

        \\
        \\

    \end{array}
}
\qquad\bf获得A和B分别为100和500
$$

<center>全部赎回</center>

---

$$
\require{enclose}
\enclose{box}{
    \begin{array}{c}
    		\\
        赎回前: \\
        x=1000 \\
        y=5000\\
        \\
        L=2236.07\\
        L_m=1000\\
        \\
    \end{array}
}
\underrightarrow{\quad\bf赎回所有流动性L-L_m\quad}
\enclose{box}{
    \begin{array}{ccccccc}
    		\\
        赎回后: \\
        L_1=1236.07 \\
				\\
        x_1=L_1*x/L\approx552.79 \\
        y_1=L_1*y/L\approx2763.93\\
        x^{1}=x-x_1=447.21\\
        y^{1}=y-y_1=2236.06\\
        L^1=L-L_1=1000\\

        \\
        \\

    \end{array}
}
\qquad\bf亏损了初始流动性销毁了L_m的流动性
$$
