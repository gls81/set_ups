# Python Notes

## Python Coding Standards

### PEP8 Type	Naming Convention	Examples

Variables: Use a lowercase single letter, word, or words. Separate words with underscores to improve readability.

    x = 1
    var = "Me"
    my_variable = "To"
    
Constants: Use an uppercase single letter, word, or words. Separate words with underscores to improve readability.

    CONSTANT = 1
    MY_CONSTANT = "Me"
    MY_LONG_CONSTANT = "To"


Functions: Use a lowercase word or words. Separate words by underscores to improve readability.

    def my_function(arg):
        #DO SOMETHING
        return


Classes: Start each word with a capital letter. Do not separate words with underscores. This style is called camel case.
    
    class Base():
    
    class SuperClass(Base):
        

Methods: Use a lowercase word or words. Separate words with underscores to improve readability.	

    class SuperClass(BaseClass):
        
        def class_method(self):
            #DO SOMETHING
            return
            
        def method(self):
            #DO SOMETHING
            return
            
            

Module	Use a short, lowercase word or words. Separate words with underscores to improve readability.	module.py, my_module.py

Package	Use a short, lowercase word or words. Do not separate words with underscores.
