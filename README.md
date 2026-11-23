# Lumi Camera — projeto organizado para Codemagic

Estrutura do app iOS para geração do projeto com XcodeGen.

```text
LumiCamera/
  *.swift
LumiCameraTests/
  CameraProfileTests.swift
project.yml
codemagic.yaml
README.md
.gitignore
```

## Build no Codemagic

O workflow `lumi-ios-build` verifica a estrutura, instala XcodeGen caso necessário, gera `LumiCamera.xcodeproj` e tenta criar um archive iOS sem assinatura.

Este archive não é um IPA instalável. Para distribuir/TestFlight, será necessário configurar assinatura Apple no Codemagic.

## Build local (Mac)

```bash
brew install xcodegen
xcodegen generate --spec project.yml
open LumiCamera.xcodeproj
```

O app requer iOS 17+. O projeto ainda precisa ser compilado e testado em macOS/Xcode.
