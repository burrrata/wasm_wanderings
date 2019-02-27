<div>
  <h1 align="center">
    This is a place to gather notes and ideas for all things WASM / Rust / Blockchain related.
  </h1>
  <div>
		<p>
    Hopefully this will lead to:
		</p>
    <ul>
      <li>
        me better understanding how WASM benefits interoperability and safety in Web3
      </li>
      <li>
        creating a tutorial to help others understand those things as well
      </li>
      <li>
        some templates and resources for people who want to build end-to-end Web3 applications using Substrate, WASM, and IPFS or other Web3 things
      </li>
  	</ul>
  </div>
</div>

<br>

<div align="center">
  <img src="https://hacks.mozilla.org/files/2017/02/01-02-perf_graph10-768x633.png">
</div>

<br>

<div align="center">
  <h1>
    WebAssembly 🕸️
  </h1>
  <p>
    Polkadot compiles to WASM. 
    Ethereum 2.0 is also exploring EWASM.
    The Web3 team seems to think it's a good idea, and so does the Rust team, and the crypto people, and pretty much everyone else.
    <br>
    So what is WASM and why should you care?
  </p>
</div>

# The TL;DR: 

WASM allows developers to write code in multiple languages then compile it to a format that plays nicely together, is fast, and works in most browsers as well as on most devices. WASM is also supported by an ecosystem much larger than the blockchain space, and this ecosystem is creating new features and tools for WASM every day. Traditionally tooling and interoperability have been a friction point in the blockchain space, but WASM could change that. 

Often this means that the sections of your code that you'll want to compile to WASM are those that are doing heavy computation, get reused often, or need to be interoperable with other systems. 


# WASM & Rust
- https://hacks.mozilla.org/2018/03/making-webassembly-better-for-rust-for-all-languages/

What does it mean for Rust to integrate with WASM?

- Rust will be able to call JavaScript functions. JavaScript will be able to call Rust functions. Rust will be able to call functions from the host platform, like alert. Rust crates will be able to have dependencies on npm packages. And throughout all of this, Rust and JavaScript will be passing objects around in a way that makes sense to both of them.
- However, don’t expect Rust WebAssembly apps to be written completely in Rust. In fact, expect the bulk of application code to be JS, even in most Rust WebAssembly applications. This is because JS is a good choice for most things. It’s quick and easy to get up and running with JavaScript. On top of that, there’s a vibrant ecosystem full of JavaScript developers who have created incredibly innovative approaches to different problems on the web. The Rust/WASM code can be used for more computation heavy functions or things that can be compiled and reused often. 


# wasm-bindgen
- https://hacks.mozilla.org/2018/04/javascript-to-rust-and-back-again-a-wasm-bindgen-tale/
- https://hacks.mozilla.org/2018/06/babys-first-rustwebassembly-module-say-hi-to-jsconf-eu/

`wasm-bindgen` erases the impedance mismatch between WebAssembly and JavaScript, ensuring that JavaScript can invoke WebAssembly functions efficiently and without boilerplate, and that WebAssembly can do the same with JavaScript functions.









# Hopefully Helpful Resources

WASM

- [Highlevel overview of WASM: where it's at (late 2018) and where it's going (2019/2020)](https://hacks.mozilla.org/2018/10/webassemblys-post-mvp-future/)
- 

Rust + WASM

- [arewewebyet](https://www.arewewebyet.org/) A compendium of resources for Rust related web dev.
- [arewewebyet WASM section](https://www.arewewebyet.org/topics/webassembly/)
- [Code for all things Rust/WASM](https://github.com/rustwasm/)
- [The Rust 🦀 and WebAssembly 🕸 Book](https://rustwasm.github.io/book/introduction.html)
- [Rust + WASM walkthrough](https://hacks.mozilla.org/2018/03/making-webassembly-better-for-rust-for-all-languages/)
- [`wasm-pack` walkthrough](https://hacks.mozilla.org/2018/04/hello-wasm-pack/)
- [`wasm-bindgen` walkthrough](https://hacks.mozilla.org/2018/04/javascript-to-rust-and-back-again-a-wasm-bindgen-tale/)

Parity Stuff To Explore

- [wasmi - WebAssembly interpreter written in Rust](https://github.com/paritytech/wasmi)
- [`parity-wasm`:WebAssembly serialization/deserialization in Rust](https://github.com/paritytech/parity-wasm)
- [`wasm-utils`: Collection of WASM utilities used in Parity and WASM contract devepment](https://github.com/paritytech/wasm-utils)

