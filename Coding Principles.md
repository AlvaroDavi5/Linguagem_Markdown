# Case Types:

- **PascalCase**: _classes_  
- **camelCase**: _functions, members, methods, attributes, parameters, variables_  
- **snake_case**: _files, database/dataset columns, objects/dicts fields_  
- **SCREAMING_CASE**: _macros, constants_  
- **kebab-case**: _ids_  

___

# Clean Code:

- Meaningful, Pronounceable, Searchable and Short but Descriptive Names
	* Context Names
	* Problem Domain Names
	* Solution Domain Names
	* Patters Names
- Class Names as Noun
- Attribute and Member Names as Adjective
- Method and Function Names as Verb
- Functions must be Modularized and have No Side Effects
- Functions must be Small and Descriptive
- Functions must do Only One Thing
- Functions must have Few Arguments
- Functions must have No Flag Arguments (Dynamic Behavior/Return)
- Functions must Avoid Unknown or Dynamic data types in their Parameters and Return
- Functions must Handle Exceptions or Error Codes and Provides their Program Flux
- Comments Don't Replace a Self-Descriptive Code
- Comments are only required for Code Headers and Description of Complex Algorithms
- Comments can be used for Warnings and TODO notes
- Comments can be used to Display Information through the IDE if it is really necessary
- Code Formatting and Modularization should help Distinguish Contexts and Functionality while maintaining Visibility
- Data Structures and Objects can be used to Represent Abstract Structures or Entities
- Data Structures Implementation must be Hidden and Interface must be Clear and Complete
- Test to Learn how to use Third-Party Code (Libs, Frameworks, Functions, Algorithms, APIs...)
- Write unit/feature/automated Tests First, Before Write Production Code
- Class Structure (in order):
	* attributes/members
		* constants
		* variables
			* statics
			* instances
	* methods/member functions
- Object-Oriented Programming:
	- Abstraction:
		* Class Should Represent a Object
		* Class Should be Small
	- Inheritance:
		* A SubClass based on a SuperClass must Inherits it Attributes and Methods
	- Encapsulation:
		* Class Methods Always must be Public
		* Class Constants (Attributes) Usually must be Public
		* Class Static and Instanced variables (Attributes) must be Private, use Class Methods to Modify Then (Getters and Setters)
	- Polymorphism:
		* _Overloading_: Overload Methods with Different Signature but Same Identifier in a Class Constructor Method
		* _Overriding_: Override Methods with the Same Signature from a SuperClass in a SubClass
	- Instantiation:
		* Class must be an Object Shape Mold
		* Object is a Class Instance
- S.O.L.I.D. Principles:
	* **Single Responsibility**: A Class must have Only One Responsibility or Represents Only One Entity
	* **Open-Closed**: Entities should be Open for Extension but must be Closed to Modification
	* **Liskov Substitution**: A Derived Class must be Replaceable with its Base Class
	* **Interface Segregation**: Segregate Interfaces as per the Requirements of Program rather than one General Purpose Implementation
	* **Dependency Inversion**: Hight-Level Classes should not depend on Low-Level Classes instead both should depend upon Abstraction.
- ...

___

# 12 Factor App:

...

___

# Design Patters:

...

___

# Architectures:

...

___

# GitFlow:

- Commits:  
	- Structure:
		```text
		:emoji: type: resumed description

		full description
		```
	- Types Nomenclature:
		* **feat**: new feature addition  
		* **fix**: bugfix or corrections  
		* **hotfix**: urgent fix  
		* **doc**: documentation updates or corrections  
		* **test**: test alterations  
		* **build**: dependencies and build files alterations  
		* **rerf**: performance alterations  
		* **refact**: code refactoration  
		* **style**: code style changes  
		* **ci**: continous integration/delivery changes  
		* **chore**: packages and configs changes  
- Branches:
	- Nomenclature: `type/CODE-descriptive_name`
	- Commom Branches:
		> _main | master_: Stable in Production
		> _rel | release_: Stable to Deploy in Production
		> _hml | homolog | staging_: Feature Validation and Tests
		> _dev | develop_: Ustable Product in Development


___

# Semantic Versioning:

- Version:
	- Nomenclature: `X.Y.Z-PR+MD`
		> **X | Major**: to incompatible API changes.  
		> **Y | Minor**: to add functionality in a backwards compatible manner.  
		> **Z | Patch**: to make backwards compatible bug fixes.  
		> **PR | Pre-Release**: to denote pre-release versions.  
		> **MD | Metadata**: to denote versions with specific metadata.  
- Changelog:
	- Structure:
		```markdown
		# Changelog

		[Semantic Versioning Specification](https://semver.org/spec/v2.0.0.html).



		## [Unreleased]

		### [X.Y.Z] - YYYY-MM-DD
		- Removed...
		- Fixed...


		## [Released]

		### [X.Y.Z] - YYYY-MM-DD
		- Added...
		- Updated...
		```




