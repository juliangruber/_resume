# resume

this is the notable creative stuff I've done in no particular order (might not be up-to-date).

## websites

### collab-tunes

The idea is to create a Digital Audio Workstation (DAW) that runs in browsers and allows for easy
collaboration, in contrast to current DAW solutions. Uses the WebAudio API!

The drum editor:

![collab-tunes](https://dl.dropbox.com/s/ntntlpaf5jm8m6z/Screen%20Shot%202012-12-09%20at%204.09.35%20PM.png)

Links:

* [drum editor](http://glowing-waterfall-3782.herokuapp.com/) (links are shareable! needs a recent chome & might take a while to load the first time)
* [synthesizer](http://juliangruber.com/synth.html) (needs a recent chrome)

Using: redis, node.js, expressjs, socket.io, stylus, jade, jquery, browserify

### alrt.io

Quickly create timers from your browsers via URLS, eg. [3s timer](http://alrt.io/3s).

Needs a browser that supports the Notification API, see [caniuse.com](http://caniuse.com/notifications).

![alrt.io](https://dl.dropbox.com/s/zx37hd68tncgmq4/Screen%20Shot%202012-12-09%20at%204.08.35%20PM.png)

Links: [alrt.io](http://alrt.io/) | [repo](https://github.com/juliangruber/alrt.io)

Using: node.js, expressjs, jade

### misc

The first I designed myself, was team leader and main coder for. The second I did as a freelancer. The third was an experiment
for Firefox OS App Days where I wanted to show simple replication patterns that work offline too.

<img src="https://dl.dropbox.com/s/4xfil4vgdyxzo9m/Screen%20Shot%202012-12-09%20at%204.10.34%20PM.png" width="33%">
<img src="https://dl.dropbox.com/s/b8ohr2te9femgwv/Screen%20Shot%202012-12-09%20at%204.11.13%20PM.png" width="33%">
<img src="https://a248.e.akamai.net/camo.github.com/6cc60fce42569e4cfbed954e52e8cb0553b01c5d/687474703a2f2f662e636c2e6c792f6974656d732f3277316a30383241314d32393147314b334d324e2f53637265656e25323053686f74253230323031332d30322d30322532306174253230342e35312e3531253230504d2e706e67" width="33%">

Links: [jakob-brucker-gymasnium.de](http://jakob-brucker-gymnasium.de/) |
[ritterschaft-zu-wasserstein.de](http://ritterschaft-zu-wasserstein.de/) | [ff-replicator.jit.su](http://ff-replicator.jit.su) & [source](https://github.com/juliangruber/ff-replicator)

## boerse go ag

I'm currently employed at [BoerseGo AG](http://www.godmode-trader.de/).

This is a realtime trading platform we've been working on:

![guidants](https://dl.dropbox.com/s/uctk4kygm2bbw85/Screen%20Shot%202012-12-09%20at%204.13.44%20PM.png)

Links: [guidants.godmode-trader.de](http://guidants.godmode-trader.de/)

## servers

### review

![review preview](https://a248.e.akamai.net/camo.github.com/054b61a93ae61870f892657f6c107f1f33eef544/687474703a2f2f662e636c2e6c792f6974656d732f334f317733593058326930733146314d323733782f53637265656e25323053686f74253230323031332d30312d3234253230617425323031322e35302e3338253230504d2e706e67)

Host reviews of your sites in different resolutions to have a quick overview of everything in every resolution.
Super useful for checking responsive designs or if everything still renders correctly.

Repo: [juliangruber/review](https://github.com/juliangruber/review) | [juliangruber/review-host](https://github.com/juliangruber/review-host)

### traffic-light

Monitor you servers with simple dynamic traffic-lights:

![preview](https://raw.github.com/juliangruber/traffic-light/master/images/green.png)

Repo: [juliangruber/traffic-light](https://github.com/juliangruber/traffic-light)

### contre

A continuous release tool that acts as a GIT repo server and lays repos out in a github-style directory structure
whenever you push to it. I created this for [component](https://github.com/component/component).

Repo: [godmodelabs/contre](https://github.com/godmodelabs/contre)

### statsc

Push stats to StatsD from the browser!

Repo: [godmodelabs/statsc](https://github.com/godmodelabs/statsc)

### multilevel

Access a levelUp-instance from multiple processes. LevelDB's design forbids you to access a database instance from multiple processes. This (wip) exports the levelUp interface 1:1.

```js
var db = multilevel.client('http://localhost:3000')
db.set('foo', 'bar')
```

Repo: [juliangruber/multilevel-http](https://github.com/juliangruber/multilevel-http), [juliangruber/multilevel](https://github.com/juliangruber/multilevel)

### dashbo

A frontend for the [graphite](http://graphite.wikidot.com/) graphing server with dashboards and other goodies.

![dashbo](https://dl.dropbox.com/s/zb45sc344kf70g2/Screen%20Shot%202012-12-09%20at%204.15.20%20PM.png)

Repo: [juliangruber/dashbo](https://github.com/juliangruber/dashbo)

## applications

### jilla

Geeking up JIRA by writing an efficient-to-use cli interface for it.

Ever wished, you could:

```bash
$ jilla ls
WDSERVICE-78 <jgruber>  !! LessLinter
PS-656       <jgruber>  !! Graphite installieren
PS-480       <pkostoff>  ! Trailing stops
```

This also does time loggin, search, resolve/close/etc.

Repo: [godmodelabs/jilla](https://github.com/godmodelabs/jilla)

### tapedeck

Run tap(e) tests in your browser with tap output in your terminal


```bash
$ tapedeck test/*.js
Open up http://localhost:13379 in your browser

TAP version 13
# editable
ok 1 input changed
ok 2 stream received data
ok 3 el changed

1..3
# tests 3
# pass  3

# ok 

$ echo $?
0
```

Repo: [juliangruber/tapedeck](https://github.com/juliangruber/tapedeck)

## libraries

Node.js libraries

### leveled

A node.js binding to [LevelDB](http://code.google.com/p/leveldb/) with focus on performance and a minimal api,
allowing you to write databases in JavaScript.

```js
var db = leveled('/tmp/db')
db.set('foo', 'bar')
```

Repo: [juliangruber/node-leveled](https://github.com/juliangruber/node-leveled)

### fwd

Taking the idea of piping streams into each other and applying that on the concept of EventEmitters.

```js
// with streams
streamA.pipe(streamB)
// with fwd
fwd(emitterA, emitterB)
```

Repo: [godmodelabs/fwd](https://github.com/godmodelabs/fwd)

### misc

* [spinner](https://github.com/godmodelabs/spinner)

![spinner](http://i.imgur.com/Iyl0d.png)

## misc

### llint.chocmixin

A [Chocolat](http://chocolatapp.com/)-Mixin that reorders less/css lines by alphabet and importance.

This uses [llint](https://github.com/juliangruber/llint) and [parseless](https://github.com/juliangruber/parseless), my
less/css parser.

Link: [mixins.chocolatapp.com](http://mixins.chocolatapp.com/mixins/20/)

### openmasse

A bookmarklet that helps with opening many links at once.

Links: [website](http://juliangruber.github.com/openmasse/) | [repo](https://github.com/juliangruber/openmasse)

### rayboy

A raytracer I wrote for educational purposes in 9th grade. It's written in C++ and can only render colored spheres.

![rayboy](http://i.imgur.com/oBHfn.png)

Repo: [juliangruber/rayboy](https://github.com/juliangruber/rayboy)

## papers

### introduction to erlang

![excerpt](http://i.imgur.com/JXGR8.png)

Download: [paper](https://dl.dropbox.com/s/cyy9iv2y1rcqa3s/Ausarbeitung.pdf?dl=1)

## artworks

### running death - the call of extinction

I created the t-shirt and designed cover and logo based on pencil drawings by a friend.

<img src="http://f.cl.ly/items/411q1L0g1b41260q2x2p/Image%202013.02.04%2010:43:08%20AM.png" width="50%">
<img src="https://dl.dropbox.com/s/dultpww5r5y4unb/artwork_stripes_finalized.jpg" width="50%">

### c'est moi:

![julian](https://secure.gravatar.com/avatar/a010d5218f2c3d194dbbac9c5d14d0ad?s=420&d=https://a248.e.akamai.net/assets.github.com%2Fimages%2Fgravatars%2Fgravatar-user-420.png)
