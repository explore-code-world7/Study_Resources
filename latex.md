
# 矩阵/vector
```latex
\begin{equation}
\begin{pmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33}
\end{pmatrix}
\begin{pmatrix}
x_1 \\
x_2 \\
x_3
\end{pmatrix}
=
\begin{pmatrix}
b_1 \\
b_2 \\
b_3
\end{pmatrix}
\end{equation}
```


# 子图并排
```latex
\begin{figure}[htbp]
	\centering
	\begin{subfigure}[b]{0.2\textwidth}
		\centering
		\includegraphics[width=0.45\textwidth]{pic/rgbimg_with_shadow.png}
		\caption{RGB images with deep shadow}
		\label{fig:image1}
	\end{subfigure}
	\begin{subfigure}[b]{0.2\textwidth}
		\centering
		\includegraphics[width=0.45\textwidth]{pic/rgbimg_without_shadow.png}
		\caption{RGB images after removing shadow}
		\label{fig:image2}
	\end{subfigure}
	\caption{Shadow Schema}
	\label{fig:subfigures}
\end{figure}
```

# table

```latex
\begin{table}[htbp] % 定义表格的位置
    \centering % 将表格居中
    \caption{不同数据集下Bert、XLNet、RoBERTa的对比} % 添加标题
    \label{tab:example} % 创建标签
    \scalebox{1.0}{
        \begin{tabular}{|c|c|c|c|}
        \hline
        accuracy & Bert & XLNet & RoBERTa \\
        \hline
        imdb &  h & 90.17 & 81.50 \\
        \hline
        sentiment\_140 & h & 85.97 & 82.36 \\ 
        \hline
        \end{tabular}
    }
\end{table}
```
