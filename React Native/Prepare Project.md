# 프로젝트 준비

## 1. React Native CLI 명령어 사용
* `react-native init [ProjectName]`

## 2. 개발 편의 위해 Typescript, Styled Components, babel-plugin-root-import 명령어 설치
* `cd [ProjectName]`
* `npm install --save styled-components`
* `npm install --save-dev typescript @types/react @types/react-native @types/styled-components babel-plugin-root-import`

## 3. Typescript 설정
* tsconfig.json 파일 생성 및 다음 내용 추가
    ```
    {
        "compilerOptions": {
            "allowJs": true,
            "allowSyntheticDefaultImports": true,
            "esModuleInterop": true,
            "isolatedModules": true,
            "jsx": "react",
            "lib": ["es6"],
            "moduleResolution": "node",
            "noEmit": true,
            "strict": true,
            "target": "esnext",
            "baseUrl": "./src",
            "paths": {
                "~/*": ["*"]
            }
        },
        "exclude": [
            "node_modules",
            "babel.config.js",
            "metro.config.js",
            "jest.config.js"
        ]
    }
    ```

## 4. 절대 경로로 컴포넌트 추가 위해 babel 설정
* babel.config.js 파일을 열고 아래와 같이 수정
    ```
    module.exports = {
        presets: ['module:metro-react-native-babel-preset'],
        plugins: [
            [
                'babel-plugin-root-import',
                {
                    rootPathPrefix: '~',
                    rootPathSuffix: 'src',
                },
            ],
        ],
    };
    ```

## 5. App.js 파일 변경 및 이동
* App.js -> App.tsx로 변경 및 src 폴더로 이동
* index.js에서 다음과 같이 import 수정
    ```
    ...
    import App from '~/App';
    ...
    ```
