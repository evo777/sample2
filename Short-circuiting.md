The && and || operators are called short-circuit operators. They will return the value of the second operand based on the value of the first operand.

The && operator is useful for checking for null objects before accessing their attributes. For example:

var name = person && person.getName();

This code is the same as:

if(person) {
	var name = person.getName();
}

In this example, if "person" evaluates to false, person.getName() will not run, so any side effects of doing so will not take effect.


The || operator is used for setting default values. For example:

var name = persons_name || "John Doe";