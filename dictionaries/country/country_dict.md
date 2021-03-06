# Country Dictionary 
**Tester:** Ambreen Hamadani

### Source of the Dictionary

This dictionary was created from a ISO Country list. 

### ISO

The International Organization for Standardization is an international Non Government, standard-setting body which promotes worldwide proprietary, industrial, and commercial standards. It is headquartered in Geneva, Switzerland, and works in 164 countries.

### Creation of the dictionary 
The country dictionary can be created using the following procedure: 
1. Create a textfile with the list of countries that you want to create a dictionary for. These may be acquired using the Wikidata Query Service. Each line of the text file should contain a single country.

2. Use the following command to create the dictionary
`amidict -v --dictionary country --directory country --input country.txt create --informat list --outformats xml,html`
(here --directory specifies the output directory) 

3. The output directory contains 2 files in xml and html format. 

4. There were, however, multiple errors and a lot of debugging may be required. The input file should not contain any errors. 

5. The output dictionary for further testing: https://github.com/petermr/openVirus/blob/master/dictionaries/test/country.xml


### Testing on a small number of countries
In order to test the query, only ten countries were taken within the test file to begin with
1. Canada
2. Japan
3. Norway
4. Wales
5. Ireland
6. United States of America
7. Denmark
8. Poland
9. Italy
10. Switzerland

Upon running the query as stated above, the following xml directory was retrieved: 

```
<?xml version="1.0" encoding="UTF-8"?>
<dictionary title="country_ten.txt">
 <entry term="canada" name="canada" id="CM.country.0"/>
 <entry term="denmark" name="denmark" id="CM.country.1"/>
 <entry term="ireland" name="ireland" id="CM.country.2"/>
 <entry term="italy" name="italy" id="CM.country.3"/>
 <entry term="japan" name="japan" id="CM.country.4"/>
 <entry term="norway" name="norway" id="CM.country.5"/>
 <entry term="poland" name="poland" id="CM.country.6"/>
 <entry term="switzerland" name="switzerland" id="CM.country.7"/>
 <entry term="united states of america" name="united states of america" id="CM.country.8"/>
 <entry term="wales" name="wales" id="CM.country.9"/>
 <query>('canada') OR ('denmark') OR ('ireland') OR ('italy') OR ('japan') OR ('norway') OR ('poland') OR ('switzerland') OR ('united states of america') OR ('wales')</query>
</dictionary>
```








