>> load prob_data401.mat
>> d=0.001;
>> dxdt_diff=diff(y)/d;
>> dxdt_grad=gradient(y)/d;
>> hold on;
>> plot(t,y,'r');
>> plot(t(1:end-1),dxdt_diff,'-g');
>> plot(t,dxdt_grad,'b');

>> d=1e-5;
t=0:d:10;
t=t+(t==0)*realmin;
fx=sin(t)./t;
y=cumtrapz(fx)*d;
plot(t,y);
yt1=find(t==4.5);
y45=y(yt1)

y45 =

1.6541


>> d=1e-5;
>> t=0:d:pi;
>> t=t+(t==0)*realmin;
>> fx=@(t)exp((sin(t)).^3);
>> s=integral(fx,0,pi)

s =

    5.1370
·ûºÅÑéËã

>> syms x;
>> fxx=exp((sin(x))^3);
>> ss=int(fxx,x,0,pi)
 
ss =
 
int(exp(sin(x)^3), x, 0, pi)






²©¿ÍµØÖ·https://i.csdn.net/#/uc/profile