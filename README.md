<div align="center">
  <br>
  <h1>🎆 Fireworks Tootcart 🎆</h1>
  <p>
    <b>A <a href="https://www.lexaloffle.com/pico-8.php">PICO-8</a> fireworks display in 262 characters.</b><br />
  <sup>(<i>279 including hashtags!</i>)</sup>
  </p>
  <p>
    <sup><a href="https://www.pico-8-edu.com/?c=AHB4YQECANtPcE5x-9nnBCcXwdnnv8EFJyTl3WmaZae-QDd-fn-OKffck8Xl3AuUZ51TnJMvLLxB1zxCEd2UJvds1A9RHnbXQN2vHJY1vTXOuqvqXyLu05V6b2yuHmj7gQVflQNt1ubFE8Sxr_xSTeZTSbSyN1KkMyvNbe0j9Dsz8U46UoWvEI6VZV1aoA1f4D4VondIVxfKok90SHTDBIaqMM6zja2ZzRmrBd3s8JTE2Eg-kQf10I3V4OSwmEGwUogZTG4Mrjbx6iuMLntoZaV8h8lyd2u6GFgH&g=w-w-w-w1HQHw-w2Xw-w3Xw-w2HQH">Live demo</a>&nsbp;&nbsp;|&nsbp;&nbsp;<a href="./main.p8">Annotated code in
    <code>main.p8</code></a></sup>
  </p>
  <br>
  <br>
  <br>
</div>

<div align="center">

![8s clip showing pixelated fireworks launching from the bottom of a 128x128 black screen, then exploding in different colours.](./firework-tootcart.gif)

</div>

```lua
r=rnd::_::cls()srand()for i=1,20 do
m=8+8*r()q=(t()/m)%1
x=64+q*256*(r()-.5)y=128+sin(q)*64*(r()+.8)s=sgn(sin(q+.8))circ(x,y,s-1,7)j=2*(q-.2)k=m*(1-(1-j)^9)for u=0,1,.1 do
circfill(x+sin(u)*k,y+cos(u)*k,s*flr(sin(q-.9)),q>.45 and 1 or 8+i%8)
end
end
flip()goto _
```
