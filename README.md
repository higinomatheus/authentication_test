# Flutter Firebase Google Sign-In App

Este é um projeto de exemplo que demonstra como implementar autenticação de login com o Google em um aplicativo Flutter utilizando o Firebase Authentication.

## ✨ Funcionalidades

- Login com conta Google
- Exibição da foto e nome do usuário
- Logout da conta Google
- Integração com Firebase Authentication

## 🛠️ Tecnologias e pacotes utilizados

- [Flutter](https://flutter.dev/)
- [Firebase Core](https://pub.dev/packages/firebase_core)
- [Firebase Auth](https://pub.dev/packages/firebase_auth)
- [Google Sign-In](https://pub.dev/packages/google_sign_in)

## 🚀 Como rodar o projeto

Siga as etapas abaixo para executar o projeto em sua máquina local:

### 1. Clone este repositório

```bash
git clone https://github.com/higinomatheus/authentication_test.git
cd authentication_test
```

### 2. Instale as dependências do Flutter

```bash
flutter pub get
```

### 3. Configure o Firebase

#### Criar um projeto no Firebase
- Acesse o Firebase Console.
- Clique em Adicionar Projeto e siga os passos.

#### Habilitar Autenticação via Google
- No painel do Firebase, vá em Authentication > Métodos de login.
- Clique em Google e ative o provedor de login com Google.
- Defina o e-mail de suporte solicitado.

#### Adicionar App Android ao Firebase
- No Firebase Console, clique em Adicionar app e escolha Android.
- Informe o Nome do pacote (exatamente como está no seu android/app/build.gradle, no campo applicationId).
- (Opcional) Informe também o apelido do app e o certificado SHA-1.

#### Como obter a chave SHA-1 no Flutter
- No terminal, navegue até a pasta android do projeto e execute:

```bash
./gradlew signingReport
```
- No Windows:

```bash
.\gradlew signingReport
```

- Procure pela seção Variant: debug ou Variant: release.
- Copie a linha que começa com SHA1:
- Exemplo de saída:

```ruby
SHA1: 12:34:56:78:9A:BC:DE:F0:12:34:56:78:9A:BC:DE:F0:12:34:56:78
```
- Cole este SHA-1 no cadastro do app Android no console do Firebase.

#### Adicionar o arquivo google-services.json
- Após registrar o app Android, o Firebase gerará um arquivo google-services.json.
- Baixe esse arquivo e coloque dentro da pasta:
```bash
android/app/
```

### 4. Execute o projeto
- Conecte seu dispositivo físico ou emulador e execute:

```bash
flutter run
```

