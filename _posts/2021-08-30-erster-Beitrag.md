### Aufgabenstellung

Es ging um einen Auftrag der in jsf erstellt werden musste. Jsf ist ein Framework welches zur Entwicklung von grafischen Benutzeroberflächen für Webanwendungen angewendet wird. 

In diesem Auftrag kann man Eigenschaften eines Charakters auswählen. Diese Eingaben mussten über mehrere Seiten weitergegeben werden. Diese mussten zu einem Namen umgewandelt werden, der einem Bild entspricht. Das Bild muss den Ausgewählten Daten entsprechen und danach dargestellt werden.

****

### Ziele

1. Ich kann ein Bild in Jsf einbinden
2. Es wird der passender Name generiert
3. Benutzereingaben werden ausgegeben

****

### Produkt

Das Endprodukt sind mehrere xhtml Seiten, die nach verschiedenen Merkmalen des zu erstellenden Charakters. Die ausgewählten Merkmale werden über die Seiten weitergegeben. Auf der letzten Seite wird ein Bild mit den Ausgewählten Merkmalen dargestellt.

Bild in Jsf einbinden:

```xml
<context-param>
        <param-name>javax.faces.WEBAPP_RESOURCES_DIRECTORY</param-name>
        <param-value>/WEB-INF/resources
        </param-value>
</context-param>
```



Code für das generieren des Namens:

```Java
public String getFilename() {
        
        String returnstring = "";
   
        if(this.haircolor != null){
            returnstring += haircolor.toCharArray()[0];
        }
        if(this.haircolor != null){
            returnstring += eyecolor.toCharArray()[0];
        }
        if(this.haircolor != null){
            returnstring += skincolor.toCharArray()[0];
        }
       
        return returnstring;
        
    }
```



Ausgabe des erstellten Charakters und die Eingaben des Benutzers:

```xhtml
<h:body>
        <h:graphicImage library="img" name="#{characterBean.filename}.png"/>
        <br/>
        <h:outputText value="Hautfarbe: #{characterBean.skincolor}"></h:outputText>
        <br></br>
        <h:outputText value="Augenfarbe: #{characterBean.eyecolor}"></h:outputText>
        <br></br>
        <h:outputText value="Haarfarbe: #{characterBean.haircolor}"></h:outputText>
    </h:body>
```



Produkt Video:

[![Youtube Video](https://img.youtube.com/vi/syNcfVKL1ss/0.jpg)](https://youtu.be/syNcfVKL1ss)

****

### Verifizierung

1. Diese Ziel wurde erreicht, wie man im oben stehenden Code sehen kann
2. Diese Ziel wurde erreicht. Im mittleren Code kann man sehen, wie der Name generiert wird
3. Dieses Ziel wurde erreicht, wie man im untersten Code sehen kann.

****

###  Reflexion

Das einbinden eines Bildes in jsf verlief ohne Probleme, da uns der Lehrer gezeigt hat, wie es gemacht wird.

Die Ausgabe der Benutzereingaben verlief auch ohne Probleme, da wir es schon im Unterricht mehrmals angeschaut haben.

Beim Generieren des Namen für das darstellen des Bildes hatte ich Probleme, da ich zuerst etwas versucht habe, dass nicht möglich war. Jedoch nachdem ich mich im Internet informiert hatte, eine Lösung gefunden habe.

##### Verbesserungsvorschlag:

Beim nächsten Mal, sich zuerst über die Themen informieren und nicht direkt ans Programmieren gehen.
