![example](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/marolive/plantuml-diagrams/master/example/example2.puml)

@startuml
autonumber
box "UK" #salmon
  participant User
  participant A
end box

User -> A: DoWork
activate A
== Initialization ==

A -> B: << createRequest >>
activate B #tomato
autonumber 15
B -> C: DoWork
activate C 
...5 minutes latter...
C --> B: WorkDone
destroy C
B --> A: RequestCreated
deactivate B
note right
  This is **bold**
  This is //italics//
  This is ""monospaced""
  This is --stroked--
  This is __underlined__
  This is ~~waved~~
end note
A -> User: Done
deactivate A
@enduml
