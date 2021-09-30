# SpringBoot_notes
In this We can have Some Important Notes about SpringBoot Basics
**Q1)Why we need no-argument constructor in SpringBoot Applications**
A:It's not mandatory to define default constructor, but if you are writing Hibernate persistent class, JPA entities, or using the Spring framework to manage object creation and wiring dependencies, you need to be a bit careful. Many of open source framework, uses reflection to create instance or Object at runtime, based upon the name of the class.

For example, When Hibernate creates an instance of entities using reflection it uses the Class.newInstance() method, which requires a no-argument constructor to create an instance. It's effectively equivalent to the new Entity().

This method throws InstantiationException if it doesn't found any no-argument constructor in the Entity class, and that's why it's advised to provide a no-argument constructor.

Btw, if you are new to the world of Hibernate then I also suggest you go through a hands-on course like these best Hibernate and JPA courses for Java developers. It's a great resource to understand the Hibernate fundamentals and advanced concepts for beginners and experienced java developers.
