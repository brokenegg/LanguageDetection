# Language Detection

Language Detection is a natural language detection library implemented in pure C#
ported from https://github.com/shuyo/language-detection.

## Abstract

  * Generate language profiles from Wikipedia abstract xml
  * Detect language of a text using naive Bayesian filter
  * 99% over precision for 53 languages

## Requires

  * .NET Standard 2.0

## Binaries

  * [NuGet Page](https://www.nuget.org/packages/BrokenEgg.LanguageDetection)

## Sample

```csharp
using LanguageDetection;

DetectorFactory.LoadProfile(profileDirectory);
Detector detector = DetectorFactory.Create();
detector.Append(text);
detector.detect();

Detector detector = DetectorFactory.Create();
detector.Append(text);
detector.GetProbabilities();
```

## Original Copyrights and License for Java implementation

Copyright (c) 2010-2014 Cybozu Labs, Inc. All rights reserved.

> Licensed under the Apache License, Version 2.0 (the "License");
> you may not use this file except in compliance with the License.
> You may obtain a copy of the License at

> http://www.apache.org/licenses/LICENSE-2.0

> Unless required by applicable law or agreed to in writing, software
> distributed under the License is distributed on an "AS IS" BASIS,
> WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
> See the License for the specific language governing permissions and
> limitations under the License.