### XSD - XML schema

```xml
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"> 
  <xsd:element name="measurements" type="measurements"/> 
  <xsd:complexType name="measurements"> 
    <xsd:sequence>
      <xsd:element name="element" maxOccurs="unbounded" type="element"/>
    </xsd:sequence>
  </xsd:complexType> 
  
  <xsd:complexType name="element"> 
    <xsd:sequence>
      <xsd:element name="data" type="data"/>
      <xsd:element name="location" type="location"/>
      <xsd:element name="time" type="xsd:dateTime"/>
    </xsd:sequence>
  </xsd:complexType>

  <xsd:complexType name="data"> 
    <xsd:sequence>
      <xsd:element name="no2" type="no2"/>
      <xsd:element name="no2_strat" type="no2"/>
      <xsd:element name="no2_trop" type="no2"/>
    </xsd:sequence>
  </xsd:complexType>

  <xsd:complexType name="no2"> 
    <xsd:sequence>
      <xsd:element name="precision" type="xsd:double"/>
      <xsd:element name="value" type="xsd:double"/>
    </xsd:sequence>
  </xsd:complexType>

  <xsd:complexType name="location"> 
    <xsd:sequence>
      <xsd:element name="latitude" type="xsd:double"/>
      <xsd:element name="longitude" type="xsd:double"/>
    </xsd:sequence>
  </xsd:complexType>
</xsd:schema>
```