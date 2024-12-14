# 🔢 Simple Calculator - My First Motoko Project 🚀
This is my first Motoko project. I created a simple calculator to demonstrate basic functionality in the Motoko programming language.

## About the Project

- **Technology Used:** [Motoko Playground](https://play.motoko.org/)
  
- **Features:**
  - Addition
  - Subtraction
  - Multiplication
  - Division
  - Clear
  
## How to Use

Simply click [this link](https://a4gq6-oaaaa-aaaab-qaa4q-cai.raw.icp0.io/?id=25x2w-paaaa-aaaab-qackq-cai&tag=1&did=c2VydmljZSA6IHsKICBib2xtZTogKGludCkgLT4gKG9wdCBpbnQpOwogIGNhcnBtYTogKGludCkgLT4gKGludCk7CiAgY2lrYXJtYTogKGludCkgLT4gKGludCk7CiAgdGVtaXpsZTogKCkgLT4gKCk7CiAgdG9wbGFtYTogKGludCkgLT4gKGludCk7Cn0K) and start using the calculator. It's straightforward and beginner-friendly!

## Screen Recording

Here's a GIF showing how I wrote this code using [Motoko Playground](https://play.motoko.org/):

![Working Demo](https://github.com/basaranseyma/Motoko_Calculator/blob/main/Motoko_Calculator.gif)

## Code 

Below is the Motoko code for the calculator:

```motoko
// hesap makinesi
// değişkenler (let -> immutable, var -> mutable)
// operatörler 
// async metodu 
// if condition

// canister => akıllı sözleşme

actor hesap_makinesi {
  var hucre: Int = 0;
  // toplama
  public func toplama(s: Int) : async Int {
    hucre += s;
    hucre
    // (Debug.print(debug_show (hucre));)
  };
  // çıkarma
  public func cikarma(s: Int) : async Int {
    hucre -= s;
    hucre
  };
  // çarpma
  public func carpma(s: Int) : async Int {
    hucre *= s;
    hucre
  };
  // bölme
  public func bolme(s: Int) : async ?Int {
    if (s == 0) {
      null
    } else {
      hucre /= s;
      ?hucre
    };
  };

  // temizle
  public func temizle() : async () {
    hucre := 0;
  };
};
