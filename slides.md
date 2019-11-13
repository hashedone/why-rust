# why Rust?

----

```cpp
if(!active.load()) {
  bool expected = false;

  std::vector<std::string> failures = checkTriger();

  if(
    !failures.empty() &&
    active.compare_exchange_weak(expected, true)
  ) {
    performAction();
  }
}
```

---

```cpp
if(!active.load()) {
  std::vector<std::string> failures = checkTriger();

  for(const auto & failure: failures) {
    bool expected = false;
    if(active.compare_exchange_weak(expected, true)) {
        performAction();
    }
  }
}
```

# Thats why Rust

---

## Disclaimer - Really Rust?

* For C(++) Devs: <span style="color: green" class="fragment">Yes</span>
* For Java/C# Devs: <span style="color: yellow" class="fragment">Maybe</span>
* For web backend Devs: <span style="color: yellow" class="fragment">Worth checking</span>
* For web frontend Devs: <span style="color: yellow" class="fragment">Worh checking</span>
* For functional Devs: <span style="color: red" class="fragment">Probably no</span>
* For Go/D Devs: <span style="color: green" class="fragment">Come on, you found time for Go/D...</span>

----

## Cargo - great toolset

* <span class="fragment">Dependency tool</span>
* <span class="fragment">Great code linter (cargo clippy)</span>
* <span class="fragment">Generate your documentation (cargo doc)</span>
* <span class="fragment">Keep your code formated (cargo fmt)</span>
* <span class="fragment">UT integrated (cargo test)</span>
* <span class="fragment">Keep your toolset updated (rustup)</span>

----

> 70 percent of all security bugs are memory safety issues

Catalin Cimpanu, Microsoft - Zero Day

Feb 11, 2019 - 15:48 GMT

---

## Static analysis build into language
### <span class="fragment">aka Borrow Checker</span>

* <span class="fragment">No dangling pointers/iterators</span>
* <span class="fragment">No `NullPointerException`</span>
* <span class="fragment">No `SegmentationFault`</span>
* <span class="fragment">No data races</span>

### <span class="fragment">And all of this with *no Garbage Collector*</span>

----

## It compiles to native
### <span class="fragment">It means it is really performant</span>
#### <span class="fragment">Sadly its proven, that sometimes it is not the best on this field</span>

----

## Learns from predecessors
* <span class="fragment">Great buildsystem</span>
* <span class="fragment">Linkage level backward compatibility...</span>
* <span class="fragment">... but syntax is a subject to evolve</span>
* <span class="fragment">Inspired with FP languages, but still stays close to metal</span>

----

## Targets many fields
* <span class="fragment">Native system language</span>
* <span class="fragment">Easy FFI via C interfaces</span>
* <span class="fragment">Works nice for embeded devices</span>
* <span class="fragment">Easy to use REST/GraphQL crates</span>
* <span class="fragment">Compiles to WASM, and easly integrates with JS</span>
* <span class="fragment">Compiles to native GPU kernels (but still with issues)</span>

----

## Active community
* <span class="fragment">Rust Wrocław - visit our Slack!</span>
* <span class="fragment">Rust users forum</span>
* <span class="fragment">Rust internals forum</span>
* <span class="fragment">Rust working groups</span>
* <span class="fragment">This week in Rust</span>
* <span class="fragment">Are we there yet?</span>

----

## Great resources
* <span class="fragment">The Book</span>
* <span class="fragment">Rust by Example</span>
* <span class="fragment">Rustling</span>
* <span class="fragment">Cargo/Rustdoc Book<span>
* <span class="fragment">Rustonomicon</span>
* <span class="fragment">CmdLine/WASM/Embeded Book</span>
* <span class="fragment">RustConf (and more) on YT</span>

----

# Learn Rust
### <span class="fragment">And become Rustacean</span>

---

## Visit us
### rust-wroclaw.pl
#### github.com/hashedone

---

# Thank you
