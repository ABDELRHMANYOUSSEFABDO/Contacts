### Clean Architecture: An iOS Project
![image](https://github.com/ABDELRHMANYOUSSEFABDO/Contacts/assets/68148770/b6378009-8cf0-449e-80c0-8bf987b09983)
We are going to structure our application in the following way:

#### System Structure
We structure the application in the following way to show intent by file / folder structure

```
-- Contacts
    │── Presentation
    │   └── Contact
    │       ├── Create
    │       │   ├── ContactCreateViewModel.swift
    │       │   └── ContactCreateView.swift
    │       ├── Edit
    │       │   ├── ContactEditViewModel.swift
    │       │   └── ContactEditView.swift
    │       └── List
    │           ├── ContactListViewModel.swift
    │           └── ContactListView.swift
    ├── Domain
    │   ├── Protocols
    │   │   ├── UseCases
    │   │   │   └── Contact
    │   │   │       ├── CreateContactUseCaseProtocol.swift
    │   │   │       ├── UpdateContactUseCaseProtocol.swift
    │   │   │       ├── DeleteContactUseCaseProtocol.swift
    │   │   │       ├── GetContactUseCaseProtocol.swift
    │   │   │       └── GetAllContactsUseCaseProtocol.swift
    │   │   └── Repositories
    │   │       └── ContactRepositoryProtocol.swift
    │   ├── Models
    │   │   └── Contact.swift
    │   ├── UseCases
    │   │   └── Contact
    │   │       ├── CreateContact.swift
    │   │       ├── UpdateContact.swift
    │   │       ├── DeleteContact.swift
    │   │       ├── GetAllContacts.swift
    │   │       └── GetContact.swift
    │   └── Repositories
    │       └── ContactRepositoryImpl.swift
    └── Data
        ├── Protocols
        │   └── ContactDataSourceProtocol.swift
        └── DataSources
            └── CoreData
            ├── Entities
            │   └── Contact.xcdatamodeld
            └── CoreDataContactDataSource.swift
-- ContactTests
    │── Mocks
    │   ├── Domain
    │   │   ├── Repositories
    │   │   │    └── MockContactRepository.swift
    │   │   └── UseCases
    │   │       └── Contact
    │   │           ├── MockCreateContact.swift
    │   │           ├── MockUpdateContact.swift
    │   │           ├── MockDeleteContact.swift
    │   │           ├── MockGetAllContacts.swift
    │   │           └── MockGetOneContact.swift  
    │   └── Data
    │       └── DataSources
    │           ├── MockContactDataSource.swift
    │           └── CoreData
    │               └── Wrappers
    │                   └── MockCoreDataWrapper.swift
    │── Presentation
    │   └── Contact
    │       ├── Create
    │       │   └── ViewModelContactCreateTests.swift
    │       ├── Edit
    │       │   └── ViewModelContactEditTests.swift
    │       └── List
    │           └── ViewModelContactListTests.swift
    ├── Domain
    │   ├── UseCases
    │   │   └── Contact
    │   │       ├── UseCaseContactCreateTests.swift
    │   │       ├── UseCaseContactUpdateTests.swift
    │   │       ├── UseCaseContactDeleteTests.swift
    │   │       ├── UseCaseContactsGetAllTests.swift
    │   │       └── UseCaseContactGetOneTest.swift
    │   └── Repositories
    │       └── ContactRepositoryTests.swift
    └── Data
        └── DataSources
            └── CoreDataContactDataSourceTests.swift

```

 


