---
title: "plotly"
<br>
output: html_document
---

##一、 plotly线图的三种画法
### 1、plot—ly函数设置type属性

```{r message=FALSE,warning=FALSE}
library(plotly)
plot_ly(cars,x=~speed,y=~dist,type='scatter',mode='lines')
```

### 2、plot—ly后置add_lines
```{r eval=FALSE}
plot_ly(cars,x=~speed,y=~dist) %>% add_lines()
```

### 3、ggplotly
```{r eval=FALSE}
p<-ggplot(cars,aes(speed,dist))+geom_line()
ggplotly(p)
```

## 二、plotly多图分布：subplot
### 1、横排分布
```{r message=FALSE}
x1<-plot_ly(cars,x=~speed,y=~dist) %>% add_lines()
x2<-plot_ly(cars,x=~speed,y=~dist) %>% add_lines()
#widths表示左右比例
subplot(x1,x2,widths = c(0.7,0.3))
```

### 2、竖排分布
```{r message=FALSE}
x1<-plot_ly(cars,x=~speed,y=~dist) %>% add_lines()
x2<-plot_ly(cars,x=~speed,y=~dist) %>% add_lines()
#heights表示左右比例
subplot(x1,x2,nrows=2,heights=c(0.3,0.7))
```
### 3、奇数个数图分布
```{r message=FALSE}
x1<-plot_ly(cars,x=~speed,y=~dist) %>% add_lines()
#plotly_empty()用空表填充
x2<-plotly_empty()
x3<-plot_ly(cars,x=~speed,y=~dist) %>% add_lines()
x4<-plot_ly(cars,x=~speed,y=~dist) %>% add_lines()
subplot(x1,x2,x3,x4,nrows=2)
```
