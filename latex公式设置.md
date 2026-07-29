---
title: "LaTeX公式设置"
date: 2023-08-30
updated: 2023-08-30
author: RUINA3S
tags: [LaTeX, 公式, 颜色, 教程]
category: [备忘�? 技术]
description: "LaTeX公式颜色及格式自用记�?
status: 记录�?
draft: true
---

# LaTeX公式设置

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





> 早知道可以调颜色就不用管上面的了，以下颜色为win10文件夹图标颜色（但看�?黄色不咋好看�?

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

