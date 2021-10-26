# next-v12-bug

```sh
pnpm i

pnpm dev
```

```sh
> pnpm --filter=foo -r dev


> next

ready - started server on 0.0.0.0:3000, url: http://localhost:3000
warn  - You have enabled experimental feature(s).
warn  - Experimental features are not covered by semver, and may cause unexpected or broken application behavior. Use them at your own risk.

event - compiled successfully in 3.2s (1515 modules)
wait  - compiling /_error...
event - compiled successfully in 322 ms (1516 modules)

<--- Last few GCs --->

[60697:0x4967150]    24587 ms: Scavenge 4046.5 (4123.3) -> 4046.0 (4131.3) MB, 5.2 / 0.0 ms  (average mu = 0.387, current mu = 0.119) allocation failure 
[60697:0x4967150]    24599 ms: Scavenge 4052.6 (4131.3) -> 4051.3 (4131.6) MB, 10.1 / 0.0 ms  (average mu = 0.387, current mu = 0.119) allocation failure 
[60697:0x4967150]    25112 ms: Scavenge 4053.6 (4131.6) -> 4052.5 (4152.6) MB, 511.8 / 0.0 ms  (average mu = 0.387, current mu = 0.119) allocation failure 


<--- JS stacktrace --->

FATAL ERROR: Reached heap limit Allocation failed - JavaScript heap out of memory
 1: 0xb02eb0 node::Abort() [node]
 2: 0xa181fb node::FatalError(char const*, char const*) [node]
 3: 0xced75e v8::Utils::ReportOOMFailure(v8::internal::Isolate*, char const*, bool) [node]
 4: 0xcedad7 v8::internal::V8::FatalProcessOutOfMemory(v8::internal::Isolate*, char const*, bool) [node]
 5: 0xea5d75  [node]
 6: 0xeb544d v8::internal::Heap::CollectGarbage(v8::internal::AllocationSpace, v8::internal::GarbageCollectionReason, v8::GCCallbackFlags) [node]
 7: 0xeb814e v8::internal::Heap::AllocateRawWithRetryOrFailSlowPath(int, v8::internal::AllocationType, v8::internal::AllocationOrigin, v8::internal::AllocationAlignment) [node]
 8: 0xe7957a v8::internal::Factory::NewFillerObject(int, bool, v8::internal::AllocationType, v8::internal::AllocationOrigin) [node]
 9: 0x11f2d56 v8::internal::Runtime_AllocateInYoungGeneration(int, unsigned long*, v8::internal::Isolate*) [node]
10: 0x15e7759  [node]
```
