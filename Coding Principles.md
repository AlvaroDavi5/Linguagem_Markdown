
# Case Types:

- **PascalCase**: _classes, interfaces, types, enums, decorators_
- **camelCase**: _functions, methods, properties, members, attributes, parameters, variables_
- **snake_case**: _files, database/dataset columns, objects/dicts fields_
- **SCREAMING_CASE**: _macros, constants_
- **kebab-case**: _ids_

___

# Clean Code and Clean Architecture:

- Meaningful, Pronounceable, Searchable and Short but Descriptive Names.
	* Context Names
	* Problem/Solution Domain Names
	* Patterns Names
- Class Names as Noun.
- Attribute and Member Names as Adjective.
- Method and Function Names as Verb.
- Functions must be Modularized and have No Side Effects.
- Functions must be Small and Descriptive.
- Functions must do Only One Thing.
- Functions must have Few Arguments.
- Functions must have No Flag Arguments (Dynamic Behavior/Return).
- Functions must Avoid Unknown or Dynamic data types in their Parameters and Return.
- Functions must Handle Exceptions or Error Codes and Provides their Program Flux.
- Comments Don't Replace a Self-Descriptive Code.
- Comments are only required for Code Headers and Description of Complex Algorithms.
- Comments can be used for Warnings and TODO notes.
- Comments can be used to Display Information through the IDE if it is really necessary.
- Code Formatting and Modularization should help Distinguish Contexts and Functionality while maintaining Visibility.
- Data Structures and Objects can be used to Represent Abstract Structures or Entities.
- Data Structures Implementation must be Hidden and Interface must be Clear and Complete.
- Test to Learn how to use Third-Party Code (Libs, Frameworks, Functions, Algorithms, APIs...).
- Write unit/feature/automated Tests First, Before Write Production Code.
- Class Structure (in order):
	* attributes/members
		* constants
		* variables
			* statics
			* instances
	* methods/member functions
- Object-Oriented Programming:
	- Abstraction:
		* Class Should Represent a Object.
		* Class Should be Small.
	- Inheritance:
		* A SubClass based on a SuperClass must Inherits it Attributes and Methods.
	- Encapsulation:
		* Class Methods Always must be Public.
		* Class Constants (Attributes) Usually must be Public.
		* Class Static and Instanced variables (Attributes) must be Private, use Class Methods to Modify Then (Getters and Setters).
	- Polymorphism:
		* _Overloading_: Overload Methods with Different Signature but Same Identifier in a Class Constructor Method.
		* _Overriding_: Override Methods with the Same Signature from a SuperClass in a SubClass.
	- Instantiation:
		* Class must be an Object Shape Mold.
		* Object is a Class Instance.
- S.O.L.I.D. Principles:
	* **Single Responsibility**: A Class must have Only One Responsibility or Represents Only One Entity.
	* **Open-Closed**: Entities should be Open for Extension but must be Closed to Modification.
	* **Liskov Substitution**: A Derived Class must be Replaceable with its Base Class.
	* **Interface Segregation**: Segregate Interfaces as per the Requirements of Program rather than one General Purpose Implementation.
	* **Dependency Inversion**: Hight-Level Classes should not depend on Low-Level Classes instead both should depend upon Abstraction.
- ...

___

# 12 Factor App:

- **Codebase**: One codebase, many deploys, strict version control.
- **Dependencies**: Explicitly declare and isolate dependencies.
- **Configuration**: Configuration stored in each environment for deploy, preferably outside the code, in environment variables.
- **Backing Services**: The application could use backing services as resources, the backing services should preferably can be represented by code abstractions and run separately (databases, caching services, queue consumers, API clients...).
- **Build, Release, Run**: The deployment process has three stages. The build generate a executable application (compiling and packaging); The release sends the build already configurated to the server; The run enable the application and it services to the final use.
- **Processes**: Keep all the processes stateless and shared-nothing. The state and others persistent data should be stored in a stateful backing service.
- **Port Binding**: The essentials services of the app should not depend of external servers and can be accessed by the other app services listening ports.
- **Concurrency**: The processes should be scaled independently and executed parallelly. The architecture should permit synchronous and asynchronous communication when neccessary.
- **Disposability**: The processes should be independent and should can be started up or shut down safely, without lost data or affect the other processes.
- **Dev/Prod Parity**: The develop, homolog and production environments should have parity and minimize gaps with continuous deployment and backing services aligned.
- **Logs**: The application logs should be stored safely and monitored to evit/detect errors.
- **Admin Processes**: Administrative tasks can be automatized to evit exteral/manual dependency.

___

# Domain-Driven Design:

The software is designed following these layers priorities:
1. Domain Layer
	- Businness Rules
	- Registered Values
2. Application Layer
	- Logic Flux
	- Authentication & Authorization
3. Infrastructure Layer
	- Backing Services Connection
4. Interface Layer
	- API Design
	- GUI Design

___

# Test-Driven Design:

- Principles
- Unit Tests
- Integration Tests
- E2E Tests
...

___

# Architectures:

- **Monolithic**: All application architecture and its layers runs as only service (logic, interface, infrastructure, auth...)
- **Microservices**: The application architecture is separated in different services, each service with its self logic, interface and infrastructure.
- **Client/Server**: The client application needs a server application to work. This server application provides all backing services integration.
- **Serverless**: The client application doesn't need a server application to work. It only uses external backing services on cloud platforms.
- **MVC**: The application has three main layers: The _Model Layer_, responsible to describe the app Businness Rules; The _View Layer_, responsible to the application interface; The _Controller Layer_, responsible to manage the requests maded by the View Layer to the Model Layer and the backing services.
- **P2P**: Descentralized network architecture, where all the clients are servers too and share data between thenselves.
- **Producer/Consumer**: The client application listen continually the server application, consuming the events produced by the server.
- **Pub/Sub**: The client application send a subscription request to the server application, which manage all the subscriptions and send specific events to the respective subscription.

___

# Design Patters:

* GoF Design Pattern:
	- State-Machines
	- Strategies
	- Factories
	- Builders
	- Adapters
	- Bridges
	- Singletons
	- Decorators
	- Interpreters
	- Iterators
	- Mediators
	- Observers
	- Visitors
	- Commands
...

___

# GitFlow:

- Commits:
	- Structure:
		```text
		:emoji: type(scope): resumed description

		full description
		```
	- Types Nomenclature:
		* **feat**: new feature addition
		* **fix**: bugfix or corrections
			* _(hotfix)_: urgent fix scope
		* **docs**: documentation updates or corrections
		* **chore**: packages and configs changes
			* _(env)_: environment configurations changes scope
		* **build**: dependencies and build files alterations
		* **test**: tests alterations
		* **perf**: performance alterations
		* **refactor**: code refactoration
		* **style**: code style and format changes
		* **ci**: continous integration/delivery changes
		* **revert**: revert existing commits
- Branches:
	- Nomenclature: `type/CODE-descriptive_name`
	- Commom Branches:
		> _main | master_: Stable in Production  
		> _rel | release_: Stable to Deploy in Production  
		> _sbx | sandbox_: Specific Feature Validation and Test  
		> _hml | homolog | staging_: Feature Validation and Tests  
		> _dev | develop_: Ustable Product in Development  


___

# Semantic Versioning:

- Version:
	- Nomenclature: `X.Y.Z-PR+MD`
		> **X | Major**: to incompatible API changes  
		> **Y | Minor**: to add functionality in a backwards compatible manner  
		> **Z | Patch**: to make backwards compatible bug fixes  
		> **PR | Pre-Release**: to denote pre-release versions  
		> **MD | Metadata**: to denote versions with specific metadata  
- Changelog:
	- Structure:
		```markdown
		# Changelog

		[Semantic Versioning Specification](https://semver.org/spec/v2.0.0.html)



		## [Unreleased]
		- ...

		### [X.Y.Z] - YYYY-MM-DD

		#### Added
		- Added...

		#### Changed
		- Updated...

		#### Fixed
		- Fixed...

		#### Removed
		- Updated...


		## [Released]

		### [X.Y.Z] - YYYY-MM-DD

		#### Added
		- Added...

		#### Changed
		- Updated...

		#### Fixed
		- Fixed...

		#### Removed
		- Updated...
		```
