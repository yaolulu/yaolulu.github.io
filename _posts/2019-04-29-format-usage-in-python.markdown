        def code_1():
            '''
            Syntax: {}.formate(value)
            :param: value can be en integer, floating point numeric constant, string, characters or even variables
            :return: Returns a formatted string with the value passed as parameter in the placeholder position
            '''
            str = "This article is written in {}.".format("Python")
            print(str)

            str = "This article is written in {}."
            print(str.format("Python"))

            print("This article is written in {}.".format("Python"))

            print ("{}, A computer science portal for geeks."
                                .format("GeeksforGeeks"))


        def code_2():
            """
            Syntax: {}{}.formate(value1, value2)
            :param: Can be integers, floating point numeric constants, strings, characters and even variables. Only difference
            is, the number of values passed as parameters in format() method must be equal to the number of placeholders created
             in the string.
            :return:
            """
            str = "{}, is a {} science portal for {}."
            print(str.format("GeeksforGeeks", "computer", "geeks"))

            print("Hi ! My name is {} and I am {} years old."
                                    .format("Shirley", 18))


        def code_3():
            """
            Formatters with positional and keyword arguments
            Syntax: {0}{1}.format(positional_arguments, keyword_argument)
            :param: (positional_arguments, keyword_argument)
            Positional_argument can be integers, floating point numeric constants, strings, characters and even variables.
            Keyword_argument is essentially a variable storing some value, which is passed as parameter.
            """
            print("{0} love {1}!!".format("GeeksforGeeks", "Geeks"))
            print("{1} love {0}!!".format("GeeksforGeeks", "Geeks"))
            print("Every {3} should know the use of {2} {1} programming and {0}."
                .format("programmer", "Open", "Source", "Operating Systems"))
            print("{gfg} is a {0} science for {1}.".format("computer", "geeks", gfg="GeeksforGeeks"))


        def code_4():
            """
            Type conversion
            Syntax: {field_name: conversion}
            """
            print ("This site is {0:f}% securely {1}!!".
                            format(100, "encrypted"))

            print ("My average of this {0} was {1:.2f}%"
                        .format("semester", 78.234876))

            print ("My average of this {0} was {1:.0f}%"
                    .format("semester", 78.234876))

            print("The {0} of 100 is {1:b}"
                .format("binary", 100))

            print("The {0} of 100 is {1:o}"
                .format("octal", 100))
        
        def code_5():
            """
            <   :  left-align text in the field
            ^   :  center text in the field
            >   :  right-align text in the field
            """
            print("{:*^21s}".format("Geeks"))
            print("{:*<21s}".format("Geeks"))
            print("{:*>21s}".format("Geeks"))

