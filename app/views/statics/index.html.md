```rust
// ./src/lib.rs

#[macro_use]
extern crate helix;

declare_types! {
    class Console {
        def log(self, string: &str) {
            println!("LOG: {}", string);
        }
    }
}
```

<h1>Ruby and Rust, sitting in a tree</h1>

<h3 class="subtitle">Helix allows you to write Ruby classes in Rust without having to write the glue code yourself.</h3>

<div class="clearfix mxn2">
  <div class="md-col md-col-6 px2">

  </div>

  <div class="md-col md-col-6 px2 column-item">
    <pre class="language-bash front-page-code-snippet">
      <code class="language-bash">
    $ irb
    >> require "console/native"
    >> Console.new.log("I'm in your Rust")
    LOG: I'm in your Rust
      <code>
    </pre>
  </div>
</div>

<div class="creatures-container">
  <img src="/images/ferris.png" class="small-creature"/>
  <a href="https://www.youtube.com/watch?v=O7oD_oX-Gio" target="_blank"><img src="/images/tiny-ruby.png" class="small-creature"/></a>
  <img src="/images/ferris.png" class="small-creature"/>
  <img src="/images/tiny-ruby.png" class="small-creature"/>
  <img src="/images/ferris.png" class="small-creature"/>
  <img src="/images/tiny-ruby.png" class="small-creature"/>
  <a href="https://www.youtube.com/watch?v=pZ7hMcePFkw" target="_blank"><img src="/images/ferris.png" class="small-creature"/></a>
  <img src="/images/tiny-ruby.png" class="small-creature"/>
  <img src="/images/ferris.png" class="small-creature"/>
</div>

<div class="clearfix mxn2">
  <div class="sm-col sm-col-4 px2">
    <h3>Ruby + Rust = ❤️</h3>
    <p>
      Helix is a bridge between Rust and Ruby (it's also a <a href="https://en.wikipedia.org/wiki/Helix_Bridge">real bridge</a>) and part of <a href="https://github.com/dherman">Dave Herman</a>'s grand plan for the Rust Bridge project. Our goal with the Helix project is to let you keep writing the Ruby you love, without fearing that you'll eventually hit a wall.
    </p>
  </div>

  <div class="sm-col sm-col-4 px2">
    <h3>Ruby at the speed of Rust</h3>
    <p>
      With Helix, you can always start with Ruby, knowing that you will always have the option to move only the CPU-intensive parts to Rust instead of rewriting your entire app in a faster language.
    </p>
  </div>

  <div class="sm-col sm-col-4 px2">
    <h3>But how?</h3>
    <p>
      Thanks to Rust's macro system, we abstracted away a lot of the verbosity and distilled it down to the parts you actually care about. Behind this deceptively small amount of code, Helix is handling a lot under the hood, such as safe, transparent type-transport between Ruby and Rust.
    </p>
  </div>
</div>

<div class="clearfix mxn2">
  <div class="col-8 px2 mx-auto hi-five">
    <img src="/images/ruby-rust-hi-five.png">
  </div>
</div>