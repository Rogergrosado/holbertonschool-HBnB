# UML Diagram

```mermaid
classDiagram
    class PresentationLayer {
        <<Interface>>
        +UserAPI()
        +PlaceAPI()
        +ReviewAPI()
        +AmenityAPI()
    }

    class BusinessLogicLayer {
        +UserModel
        +PlaceModel
        +ReviewModel
        +AmenityModel
    }

    class PersistenceLayer {
        +DatabaseAccess()
    }

    PresentationLayer --> BusinessLogicLayer : Facade Pattern
    BusinessLogicLayer --> PersistenceLayer : Database Operations
```

