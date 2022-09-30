# Pipenv

> 가상환경에서 패키지를 관리할 수 있게 해 주는 도구

## 설치

> 주의 : python이 설치되어 있어야 한다.

`pip install pipenv`

## 사용

-   ### 해당 프로젝트 루트 디렉토리로 이동한다
-   ### pipenv를 사용하여 가상환경을 만든다

    -   python 버전 3을 사용하고 싶을 때

        `pipenv --three`

    -   python 특정 버전을 사용하고 싶을 때

        `pipenv --python [버전]`

-   ### 가상환경에 진입한다

    > 가상환경 진입은 디렉토리에 들어갈 때마다 해야 한다.

    `pipenv shell`

-   ### 패키지를 설치 혹은 제거한다

    `pipenv install [패키지 이름] [옵션]`

    `pipenv uninstall [패키지 이름]`

## [옵션]

1. ### 설치 옵션

    - --dev

        pipfile의 [dev-packages]에 패키지를 추가한다.
