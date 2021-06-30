``` ini

BenchmarkDotNet=v0.13.0, OS=Windows 10.0.18363.1256 (1909/November2019Update/19H2)
Intel Core i7-10510U CPU 1.80GHz, 1 CPU, 8 logical and 4 physical cores
.NET SDK=5.0.301
  [Host]     : .NET 5.0.7 (5.0.721.25508), X64 RyuJIT
  DefaultJob : .NET 5.0.7 (5.0.721.25508), X64 RyuJIT


```
|               Method |      Mean |     Error |    StdDev | Ratio | Rank |  Gen 0 | Gen 1 | Gen 2 | Allocated |
|--------------------- |----------:|----------:|----------:|------:|-----:|-------:|------:|------:|----------:|
|      GetYearFromSpan |  38.19 ns |  0.811 ns |  1.239 ns |  0.07 |    1 |      - |     - |     - |         - |
| GetYearFromSubstring |  51.58 ns |  1.028 ns |  1.718 ns |  0.10 |    2 | 0.0076 |     - |     - |      32 B |
|     GetYearFromSplit | 176.05 ns |  3.406 ns |  5.596 ns |  0.33 |    3 | 0.0381 |     - |     - |     160 B |
|  GetYearFromDateTime | 539.69 ns | 10.567 ns | 17.064 ns |  1.00 |    4 |      - |     - |     - |         - |
