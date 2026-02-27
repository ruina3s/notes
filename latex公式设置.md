---
title: latex自用公式记录格式
date: 2023.8.30 15:00:00
tab: 
---

$$
\color{black}{黑色}\color{red}{红色}\color{green}{绿色}\color{blue}{蓝色}
\color{white}{白色}\color{cyan}{苍色}\color{magenta}{紫粉色}\color{yellow}{黄色}
$$

```latex
$$
\color{black}{黑色}\color{red}{红色}\color{green}{绿色}\color{blue}{蓝色}\color{white}{白色}\color{cyan}{苍色}\color{magenta}{紫粉色}\color{yellow}{黄色}
$$				
```

$$
\fbox{test} \\
\textcolor[gray]{0.8}{test} \\
\colorbox{red}{test}\\
\fcolorbox{blue}{yellow}{\textcolor{blue}{蓝框、黄底、蓝字}}\\
$$

```latex
$$
\fbox{test} \\
\textcolor[gray]{0.8}{test} \\
\colorbox{red}{test}\\
\fcolorbox{blue}{yellow}{\textcolor{blue}{蓝框、黄底、蓝字}}
$$					
```





> 早知道可以调颜色就不用管上面的了，以下颜色为win10文件夹图标颜色（但看这*黄色不咋好看）

$$
\color{#fee082}{test}\\
\framebox[10]{Test box}\\
\fcolorbox{#000000}{#00ff00}{\textcolor{#0000ff}{test}}\\
\color{blue}{ 
	\framebox[1]{ 
		\colorbox{red}{
			\color{green}{test}
        }
	}
} \\
\color{blue}{ 
	\fbox{ 
		\colorbox{red}{
			\color{green}{test}
        }
	}
}
$$

```latex
\color{#fee082}{test}\\
\framebox[10]{Test box}\\
\fcolorbox{#000000}{#00ff00}{\textcolor{#0000ff}{test}}\\
\color{blue}{ 
	\framebox[1]{ 
		\colorbox{red}{
			\color{green}{test}
        }
	}
} \\
\color{blue}{ 
	\fbox{ 
		\colorbox{red}{
			\color{green}{test}
        }
	}
}
```

