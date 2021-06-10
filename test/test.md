# Reconnect to last conected workspace

## Introduction
* Websocket 으로 로그인 상태 정보를 서버에 전달하는 부분이 추가됨   
* 로그인 상태 정보 Request 양식에 workspace id 가 필요함   
* Remote HoloLens2 에서는 로그인할 때 workspace id 가 null 임   
* 모바일 앱과 웹에서 로그인할 때 가장 최근에 접속한 workspace 로 자동 접속됨   
* Remote HoloLens2 에서도 로그인할 때 가장 최근에 접속한 workspace id 가 필요함   

## Requirements
* 로그인할 때 마지막으로 접속했던 workspace 에 자동으로 접속 및 workspace id 자동 갱신

## Design
* workspace 선택 버튼 누를 때 Config.json 에 해당 workspace id 저장    
* 로그인 버튼 누를 때 config.json 에 workspace id 가 있으면 해당 workspace id 갱신 및 자동으로 workspace 선택 버튼 Invoke   

![Activity Diagram](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/cjLee-VIRNECT/plantUML-test/main/test/ActivityDiagram.wsd)