# Google TypeScript style — throughline source

This document is **generated from the graph** by `tl docs`; `tl docs --check` gates it in CI. The prose headings are hand-owned — everything between `tl:*` markers is injected from the YAML items, so the published spec can never drift from the graph.

This source re-expresses the **Google TypeScript Style Guide** as a grounded IDD graph: each major section is a `user_requirement`, and every individual rule is a `system_requirement` that `implements` its section. The guide reference lives in `attrs.source_ref`; the throughline UIDs are this source's own and immutable — a consumer cites a rule as `ts:SR-0001`, never by section name.

It carries
<!-- tl:count type == 'user_requirement' -->
11
<!-- tl:end --> sections and
<!-- tl:count type == 'system_requirement' -->
68
<!-- tl:end --> style rules.

## Purpose

<!-- tl:item INT-0001 -->
**INT-0001 — TypeScript is written in one consistent, safe, maintainable style** — `intent`, status `approved`

> The Google TypeScript Style Guide exists so that TypeScript across a large codebase reads as though written by one author: consistent structure, naming and language-feature choices, biased towards the safe and statically checkable subset of the language, so that any engineer can read and change code they did not write.

**source_ref**: Google TS Style Guide
<!-- tl:end -->

## Source File Basics

<!-- tl:item UR-0001 -->
**UR-0001 — Source File Basics** — `user_requirement`, status `approved`

> Rules governing file encoding, whitespace and escape sequences.

*Derives from:* INT-0001

**source_ref**: Google TS Style Guide: Source File Basics
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Google TS Style Guide: Source File Basics') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0001 | system_requirement | approved | Encode source files in UTF-8 |
| SR-0002 | system_requirement | approved | Use only the ASCII space for in-line whitespace |
| SR-0003 | system_requirement | approved | Prefer named escape sequences over numeric escapes |
| SR-0004 | system_requirement | approved | Use actual Unicode characters for printable non-ASCII |
<!-- tl:end -->

## Source File Structure

<!-- tl:item UR-0002 -->
**UR-0002 — Source File Structure** — `user_requirement`, status `approved`

> Rules governing the order of a file's contents, imports, exports and the use of modules over namespaces.

*Derives from:* INT-0001

**source_ref**: Google TS Style Guide: Source File Structure
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Google TS Style Guide: Source File Structure') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0005 | system_requirement | approved | Order file contents and separate sections with one blank line |
| SR-0006 | system_requirement | approved | Use ES module syntax exclusively |
| SR-0007 | system_requirement | approved | Use named exports, never default exports |
| SR-0008 | system_requirement | approved | Choose named or namespace imports by usage |
| SR-0009 | system_requirement | approved | Prefer relative import paths within a project |
| SR-0010 | system_requirement | approved | Do not export mutable bindings with export let |
| SR-0011 | system_requirement | approved | Do not use container classes of static members for namespacing |
| SR-0012 | system_requirement | approved | Use import type and export type for type-only symbols |
<!-- tl:end -->

## Variables and Literals

<!-- tl:item UR-0003 -->
**UR-0003 — Variables and Literals** — `user_requirement`, status `approved`

> Rules governing variable declaration and array, object, string and number literals.

*Derives from:* INT-0001

**source_ref**: Google TS Style Guide: Language Features — Variables and Literals
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Google TS Style Guide: Language Features — Variables and Literals') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0013 | system_requirement | approved | Declare variables with const or let, never var |
| SR-0014 | system_requirement | approved | Declare one variable per statement |
| SR-0015 | system_requirement | approved | Initialise arrays with literals, not the Array constructor |
| SR-0016 | system_requirement | approved | Only spread iterables into an array literal |
| SR-0017 | system_requirement | approved | Create objects with literals, not the Object constructor |
| SR-0018 | system_requirement | approved | Only spread objects into an object literal |
| SR-0019 | system_requirement | approved | Use single quotes and template literals for strings |
| SR-0020 | system_requirement | approved | Parse numbers with Number() and check for NaN |
| SR-0021 | system_requirement | approved | Do not instantiate primitive wrapper objects |
<!-- tl:end -->

## Classes

<!-- tl:item UR-0004 -->
**UR-0004 — Classes** — `user_requirement`, status `approved`

> Rules governing class declarations, members, visibility and accessors.

*Derives from:* INT-0001

**source_ref**: Google TS Style Guide: Language Features — Classes
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Google TS Style Guide: Language Features — Classes') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0022 | system_requirement | approved | Do not end a class declaration with a semicolon |
| SR-0023 | system_requirement | approved | Omit an empty or purely delegating constructor |
| SR-0024 | system_requirement | approved | Mark never-reassigned properties readonly |
| SR-0025 | system_requirement | approved | Use parameter properties over manual field plumbing |
| SR-0026 | system_requirement | approved | Use TypeScript visibility, not JavaScript private fields |
| SR-0027 | system_requirement | approved | Limit visibility and never use a redundant public modifier |
| SR-0028 | system_requirement | approved | Prefer module-local functions to private static methods |
| SR-0029 | system_requirement | approved | Keep getters pure and side-effect free |
| SR-0030 | system_requirement | approved | Never manipulate prototypes directly |
<!-- tl:end -->

## Functions

<!-- tl:item UR-0005 -->
**UR-0005 — Functions** — `user_requirement`, status `approved`

> Rules governing function declarations, arrow functions and this.

*Derives from:* INT-0001

**source_ref**: Google TS Style Guide: Language Features — Functions
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Google TS Style Guide: Language Features — Functions') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0031 | system_requirement | approved | Prefer function declarations for named functions |
| SR-0032 | system_requirement | approved | Use arrow functions instead of function expressions |
| SR-0033 | system_requirement | approved | Do not use this outside a class or bound arrow function |
| SR-0034 | system_requirement | approved | Use rest parameters instead of arguments |
| SR-0035 | system_requirement | approved | Use a concise arrow body only when the value is used |
<!-- tl:end -->

## Control Structures

<!-- tl:item UR-0006 -->
**UR-0006 — Control Structures** — `user_requirement`, status `approved`

> Rules governing equality, blocks, iteration, switch, exceptions and assertions.

*Derives from:* INT-0001

**source_ref**: Google TS Style Guide: Language Features — Control Structures
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Google TS Style Guide: Language Features — Control Structures') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0036 | system_requirement | approved | Always use === and !== |
| SR-0037 | system_requirement | approved | Always brace control-flow blocks |
| SR-0038 | system_requirement | approved | Iterate arrays with for...of and dicts with guarded for...in |
| SR-0039 | system_requirement | approved | Give every switch a final default that does not fall through |
| SR-0040 | system_requirement | approved | Throw only Error instances |
| SR-0041 | system_requirement | approved | Avoid unexplained type and non-null assertions |
| SR-0042 | system_requirement | approved | Keep try blocks focused on throwing code |
<!-- tl:end -->

## Disallowed Features

<!-- tl:item UR-0007 -->
**UR-0007 — Disallowed Features** — `user_requirement`, status `approved`

> Language and platform features that must not be used.

*Derives from:* INT-0001

**source_ref**: Google TS Style Guide: Language Features — Disallowed Features
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Google TS Style Guide: Language Features — Disallowed Features') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0043 | system_requirement | approved | End every statement with a semicolon |
| SR-0044 | system_requirement | approved | Use a plain enum, not const enum |
| SR-0045 | system_requirement | approved | Do not use eval or the Function constructor |
| SR-0046 | system_requirement | approved | Do not use with, debugger, or non-standard features |
| SR-0047 | system_requirement | approved | Do not modify builtins or add globals |
<!-- tl:end -->

## Naming

<!-- tl:item UR-0008 -->
**UR-0008 — Naming** — `user_requirement`, status `approved`

> Rules governing the casing and choice of identifiers.

*Derives from:* INT-0001

**source_ref**: Google TS Style Guide: Naming
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Google TS Style Guide: Naming') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0048 | system_requirement | approved | Name types in UpperCamelCase |
| SR-0049 | system_requirement | approved | Name values in lowerCamelCase |
| SR-0050 | system_requirement | approved | Name global constants in CONSTANT_CASE |
| SR-0051 | system_requirement | approved | Treat acronyms as whole words when casing |
| SR-0052 | system_requirement | approved | Do not use underscore affixes or opt_ prefixes |
| SR-0053 | system_requirement | approved | Use descriptive, unambiguous names |
<!-- tl:end -->

## Type System

<!-- tl:item UR-0009 -->
**UR-0009 — Type System** — `user_requirement`, status `approved`

> Rules governing type inference, nullability, interfaces, arrays and the any/unknown types.

*Derives from:* INT-0001

**source_ref**: Google TS Style Guide: Type System
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Google TS Style Guide: Type System') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0054 | system_requirement | approved | Rely on inference for trivial types |
| SR-0055 | system_requirement | approved | Keep null and undefined out of type aliases |
| SR-0056 | system_requirement | approved | Prefer optional members to a \|undefined union |
| SR-0057 | system_requirement | approved | Use interfaces for object types |
| SR-0058 | system_requirement | approved | Use T[] for simple arrays and Array<T> for complex elements |
| SR-0059 | system_requirement | approved | Prefer unknown to any |
| SR-0060 | system_requirement | approved | Use lowercase primitive types, never wrapper types |
| SR-0061 | system_requirement | approved | Prefer Map, Set and Record to index-signature objects |
<!-- tl:end -->

## Comments and Documentation

<!-- tl:item UR-0010 -->
**UR-0010 — Comments and Documentation** — `user_requirement`, status `approved`

> Rules governing JSDoc, implementation comments and their formatting.

*Derives from:* INT-0001

**source_ref**: Google TS Style Guide: Comments and Documentation
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Google TS Style Guide: Comments and Documentation') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0062 | system_requirement | approved | Use JSDoc for documentation and // for implementation notes |
| SR-0063 | system_requirement | approved | Write JSDoc in Markdown with one tag per line |
| SR-0064 | system_requirement | approved | Document exported symbols where their use is not obvious |
| SR-0065 | system_requirement | approved | Do not box comments in ASCII art |
<!-- tl:end -->

## Toolchain Requirements

<!-- tl:item UR-0011 -->
**UR-0011 — Toolchain Requirements** — `user_requirement`, status `approved`

> Rules governing type checking and conformance.

*Derives from:* INT-0001

**source_ref**: Google TS Style Guide: Toolchain Requirements
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Google TS Style Guide: Toolchain Requirements') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0066 | system_requirement | approved | All code must pass standard type checking |
| SR-0067 | system_requirement | approved | Do not suppress type errors |
| SR-0068 | system_requirement | approved | Abide by conformance rules |
<!-- tl:end -->

