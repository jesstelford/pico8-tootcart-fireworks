# Fireworks Tootcart

A fun little code golf exercise to write a
[PICO-8](https://www.lexaloffle.com/pico-8.php) fireworks display in under 280
characters (_279 including hashtags!_).

```lua
::_::cls()srand()r=rnd
for i=1,20 do
m=8+8*r()q=(t()/m)%1
x=64+q*256*(r()-.5)y=128+sin(q)*64*(r()+.8)s=sgn(sin(q+.8))circ(x,y,s-1,7)j=2*(q-.2)k=m*(1-(1-j)^9)for u=0,1,.1 do
circfill(x+sin(u)*k,y+cos(u)*k,s*flr(sin(q-.9)),q>.45 and 1 or 8+(i/4)%8)
end
end
flip()goto _
-- #tootcart #pico8 #lua
```

👉 [**See the demo**](https://www.pico-8-edu.com/?c=AHB4YQEXAPanBPcWwc3Hv8H6fPIGVz-A4VlWXVVU1czpL1DNnx_ec8o992Rt2b5AedY5xTn5xMQbdM0jFNFNaXLPRv0Q5WF3DdT9ymFZ01vjrLuq-iXiPl0J98bm4r7Nu37BWAsLcRf36XlZPyYwEETnRccZaaPSGNgbGp2ZS2amFqeKoY2kHnmElZGpdiUdqcJXCPfKcqa0QBs_wIGJIMk7pEMLZdEnkiSyIbtDy0G_s6c30sYLG-FQtrQ7ZbW2CIfSnYV2sC0XZifL2S4ZfITZZQ8tLbXvUJfPMLNd7M7nM0FzYJYFxdb8dJNldd6FI1k2MNgC&g=w-w-w-w1HQHw-w2Xw-w3Xw-w2HQH)

👉 [Annotated code in `main.p8`](./main.p8)

![8s clip showing pixelated fireworks launching from the bottom of a 128x128
black screen, then exploding in different colours.](./firework-tootcart.gif)
