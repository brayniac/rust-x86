# x86 / amd64 library [![Build Status](https://travis-ci.org/gz/rust-x86.svg)](https://travis-ci.org/gz/rust-x86) [![Crates.io](https://img.shields.io/crates/v/x86.svg)](https://crates.io/crates/x86) [![docs.rs/x86](https://docs.rs/x86/badge.svg)](https://docs.rs/crate/x86/)


Library to program x86 (amd64) hardware. Contains x86 specific data structure descriptions, data-tables, as well as convenience function to call assembly instructions typically not exposed in higher level languages.

Currently supports
  * I/O registers
  * Control registers
  * MSR registers
  * Segmentation
  * Descriptor-tables (GDT, LDT, IDT)
  * IA32-e page table layout
  * Interrupts (with xAPIC and x2APIC registers)
  * Task state
  * Performance counter information
  * Intel SGX: Software Guard Extensions
  * Random numbers (rdrand, rdseed)
  * Time (rdtsc, rdtscp)
  * Querying CPUID (uses [raw_cpuid](https://github.com/gz/rust-cpuid) library)
  * Transactional memory (Intel RTM and HLE)

This library depends on libcore so it can be used in kernel level code.

## Features

  * performance-counter: Includes the performance counter information. Note this feature
    can increase compilation time significantly due to large, statically generated hash-tables
    that are included in the source. Therefore, it is disabled by default.

## Documentation
 * [API Documentation](https://docs.rs/crate/x86/)
