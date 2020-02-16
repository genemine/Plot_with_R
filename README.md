# Plot_with_R


## Lines in groups: ggplot

An example to plot multiple lines in one plot with ggplot.

```bash
pdf("out.pdf")
# data
x=c(1:10,1:10)
y=c(rnorm(10),rnorm(10,mean=2))
group=c(rep(1,times=10),rep(2,times=10))
thisdf=data.frame(x=x,y=y,group=group)

# plot
ggplot(thisdf, aes(x=x, y=y,group=group,colour=group))+
  geom_line(cex=1)+
  theme(axis.text.x = element_text(size=20),axis.text.y = element_text(size=20),axis.title=element_text(size=20))+
  xlim(0,10)+
  xlab("xlabel")+
  ylab("ylabel")

dev.off()

```
