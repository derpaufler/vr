Dieses Tutorial ist eine Übersetzung und Anpassung der Tutorials von PumkinSpice und monstermac77:
https://github.com/PumkinSpice/MixedVR/wiki/ReadMe
https://github.com/monstermac77/vr
Mit Zustimmung von monstermac77 fasse ich alle Schritte auf Deutsch zusammen und stelle euch im Laufe des Tutorials eine Anpassung seines Tools "MixedVR Manager" bereit.

======

Video-Tutorial: 

In diesem Tutorial zeige ich euch, wie ihr die HP Reverb G2 mit den Index Controllern koppeln könnt.

Ich werde euch zeigen, dass es sehr einfach umzusetzen ist, wenn man diesem Tutorial folgt. Wichtig ist natürlich, dass ihr keinen Schritt auslasst und wirklich alles genau so macht, wie ich es euch zeige und beschreibe. Schritte auszulassen, weil man denkt, dass man dies und jenes schon vorher erledigt hätte oder man etwas als für nicht notwendig erachte, wird im späteren Verlauf ggf. zu Problemen führen.

Sobald ihr es einmal eingerichtet habt, braucht ihr danach nichts mehr zu machen. Wenn ihr euch jetzt direkt zum Beginn dieses Tutorials fragt, dass die Index Controller doch irgendwann wegdriften, da sich die Koordinaten der HP Reverb G2 von Zeit zu Zeit ändern, dann werde ich euch ebenfalls zeigen, wie einfach und schnell ihr dies wieder beheben könnt. Und das in der Regel ohne G2-Controller zum erneuten kalibrieren.

Mein persönliches Ziel war es, die HP Reverb G2-Controller vollständig zu ersetzen. Nicht etwa, weil ich das Tracking oder die Controller selbst so schlecht finden würde, nein, im Gegenteil, jedoch sind die Index Controller einfach noch viel besser. Das gilt für mich auch im Vergleich zu den Oculus Touch-Controllern.

Außerdem war es eine Bedingung, dass ich die HP Reverb G2 auch jederzeit wieder ohne das Lighthouse-Tracking, d.h. wieder normal mit den G2-Controllern, benutzen kann, ohne, dass ich viel herumstellen muss. Da ich zwei Playspaces habe, ist das wichtig für mich.

Weiter entpuppt sich die HP Reverb G2 dann mit seinen kombinierbaren Tracking-Systemen als richtiger Allrounder, da man bei Lighthouse-HMDs immer die Basisstationen braucht, und das ist wirklich sehr umständlich. Natürlich wird die G2 nicht so portabel wie eine Quest 2, und schon gar nicht wird sie kabellos, jedoch ist diese Lösung für verschiedene Playspaces wirklich interessant.

All dies ist erst durch die wirklich engagierten Tüftler auf Reddit möglich gewesen. Besucht also bei weiteren Fragen nicht nur unseren Discord, sondern auch den Subreddit MixedVR. 

Vielen Dank an dieser Stelle besonders an die Nutzer monstermac77, pushrax, PumpkinSpice, Tetracyclic und die Programmierer der OVR Advanced Settings. Vor allem monstermac77 hat mit mir persönlich über die eine oder andere Sache diskutiert.

Nun genug des Vorworts! Steigen wir in das Tutorial ein.

Als Voraussetzung braucht ihr selbstredend die HP Reverb G2, die Index Controller sowie mindestens zwei Lighthouse-Base-Stations der Version 1.0 oder 2.0. Ob diese von Valve oder HTC sind, ist nicht relevant. Was nicht so offensichtlich ist, ist die Tatsache, dass man für jeden der beiden Index Controller jeweils einen Bluetooth Low Energy-Dongle benötigt. Leider kann man dafür nicht irgendeinen Dongle benutzen, sondern man braucht entweder zwei offizielle HTC Vive Tracker Dongles oder zwei Steam Controller Dongles. Beide sind zurzeit leider nicht ohne weiteres zu kaufen. Schaut immer wieder bei TundraLabs oder auf eBay und eBay Kleinanzeigen vorbei.

Ihr könnt natürlich auch HTC Vive Tracker kaufen, da dort die Dongles bereits mitgeliefert werden, jedoch kosten diese je ca. EUR 160,-, und die Tracker könnt ihr nicht parallel zu den Index Controllern damit koppeln. Daher würde ich davon abraten, die Tracker nur wegen der Dongles zu kaufen.

Falls ihr zwei Steam Controller Dongles verwenden möchtet, müsst ihr diese flashen. Danach sind diese nicht mehr zum Steam Controller kompatibel. Die Anleitung dafür findet ihr ganz unten, jedoch habe ich dies selbst nicht getestet und kann daher nicht dabei helfen.

Es ist zu empfehlen, die Vive Tracker Dongles unbedingt in USB 2.0-Ports zu betreiben, da USB 3.2-Ports zu Interferenzen mit dem Funksignal führen können. Nutzt daher auch unbedingt jeweils eine USB 2.0-Verlängerung je Dongle, sodass diese möglichst nah bei euch sind und jeweils möglichst weit voneinander entfernt sind.

Für den besten Komfort braucht euer PC selbst noch mindestens Bluetooth 4.0 mit genügend Reichweite, um die Lighthouse-Basisstationen zu erreichen. Gerade kleine Bluetooth-Dongles haben hier oft mit Reichweite zu kämpfen. Falls ihr jedoch kein Bluetooth habt, braucht ihr nicht unbedingt einen Dongle zu kaufen. Dazu später mehr.

Alle Links zu den Quellen und zu Dingen, die ihr braucht oder kaufen müsst, findet ihr ganz unten.

Neben der Hardware brauchen wir auch einiges an Software. Die G2 muss natürlich bereits konfiguriert und eingerichtet sein. Außerdem muss Steam und SteamVR installiert sein, natürlich auch der Windows Mixed Reality for SteamVR-Treiber. Des Weiteren ist noch folgende Gratis-Software herunterzuladen und sofort danach zu installieren: Die OVR Advanced Settings aus dem Steam Store und den OpenVR-SpaceCalibrator von GitHub.

Beginnen wir also mit der Einrichtung.

Zieht zunächst den Stromstecker der G2 aus der Steckdose, damit sich diese nicht ständig dann einschaltet, wenn wir sie noch nicht brauchen. Vorher schließt ihr das WMR-Portal, falls es geöffnet ist, damit die G2 sauber ausgeschaltet wird. Hier kann ich übrigens einen Smart Home-Plug oder eine Funksteckdose empfehlen. Dies ist die beste und zuverlässigste Methode, damit die G2 keine Fehler auswirft und auch immer nur dann eingeschaltet ist, wenn wir sie brauchen.

Danach steckt ihr einen der beiden Dongles samt der empfohlenen USB-Verlängerung an euren PC. Dieser sollte dann von Windows erkannt werden. Wartet ab, bis dieser "eingerichtet wurde und verwendet werden kann".

Öffnet Steam und SteamVR. Dass kein VR-Headset angeschlossen ist, ist richtig. Klickt in SteamVR auf dem Desktop auf Einstellungen, Geräte, Controller koppeln. Wählt die Valve Index Controller aus und befolgt die Anweisungen auf dem Bildschirm zum Koppeln eines der beiden Controller. Sobald der Controller gekoppelt ist, bestätigt die Kopplung mit "OK" und schaltet den Index Controller aus. Danach zieht ihr den Dongle vom PC ab. Es ist übrigens nicht relevant, in welchen Port ihr die Dongles später wieder einsteckt, solange es eben immer der empfohlene USB 2.0-Port ist.

Danach wiederholt ihr das ganze erneut mit dem zweiten Dongle und dem zweiten Controller.

Wenn die Kopplung abgeschlossen ist, bestätigt ihr auch hier den Vorgang mit "OK" und schaltet den Index Controller aus. Ihr könnt jetzt den ersten Dongle wieder einstecken und danach beide Controller einschalten. Beide Controller sollten nun als verbunden angezeigt werden. Falls ihr bereits Lighthouse-Basisstationen auf euch gerichtet habt und diese eingeschaltet sind, werden auch diese schon angezeigt.

Ansonsten könnt ihr das nun nachholen. Schaltet die Lighthouse-Basisstationen ein. Falls sie sich im Schlafmodus befinden, trennt den Strom für einige Sekunden und verbindet diese erneut.

Wichtig ist auch hier: Die Lighthouse-Basisstationen müssen bereits montiert sein. Ein späteres Verschieben sorgt dafür, dass die meisten Schritte umsonst waren und wiederholt werden müssen.

Jetzt werden schonmal alle Lighthouse-Geräte angezeigt und sind erfolgreich verbunden.

Übrigens: Falls die Controller ein Firmware-Update benötigen, so führt dieses durch. Bei den Basisstationen wird bei der Version 1.0 wohl davon abgeraten, bei den 2.0-Geräten jedoch nicht. Wieso das so ist, kann ich nicht sagen. Wenn jedoch auch ohne Firmware-Update am Ende alles funktioniert, könnt ihr euch das Update sowieso sparen. Never change a running system.

Jetzt schaltet ihr die Index Controller aus, lasst jedoch alles eingesteckt und die Basisstationen eingeschaltet.

Immer noch auf dem Desktop, geht in SteamVR auf Einstellungen, Start/Beenden und dann auf "Overlay-Anwendungen beim Starten auswählen". Schaltet "Space Calibrator" und "OVR Advanced Settings" auf "An" und alles andere, insbesondere fpsVR erstmal auf "Aus". Ganz am Ende könnt ihr eure persönlichen Overlay-Anwendungen wie z.B. fpsVR, die ihr jetzt evtl. ausgeschaltet habt, wieder einschalten.

Schaltet außerdem in den Einstellungen unter Controller die Option ein, dass die Index Controller beim Schließen von SteamVR automatisch ausgeschaltet werden.

Beendet nun SteamVR.

Schaltet nun eure HP Reverb G2 wieder ein und wartet, bis sich das WMR-Portal geöffnet hat.

Im WMR-Portal müsst ihr die Raumbegrenzung einschalten und diese einrichten. Dies macht ihr nun auch dann, wenn ihr sie zuvor bereits eingerichtet habt. Es ist sehr wichtig, dass ihr dies sorgfältig macht, um später zu prüfen, ob alles gut funktioniert. Stellt außerdem danach sicher, dass eure Bodenhöhe stimmt. Pro-Tipp hier: Legt einen Controller auf den Boden und schaut beim Verstellen der Höhe auf den Controller. Wird der Controller vom Boden verdeckt, wisst ihr, wie ihr die Bodenhöhe einstellen müsst.

Öffnet SteamVR aus dem Cliffhouse heraus und testet vorsichtig, ob eure Raumbegrenzung funktioniert. Diese muss sowohl durch das HMD als auch durch die Controller ausgelöst werden. Wenn ihr die Raumbegrenzung seht und alles in Ordnung ist, so war die Einrichtung erfolgreich. Legt euch jetzt die Steam Controller vor euch auf den Boden. Legt den linken G2 Controller beiseite und schaltet ihn vorher ab, indem ihr den Windows-Button gedrückt haltet.

Öffnet das SteamVR Dashboard, klickt unten links auf die drei Punkte und öffnet Space Calibrator. Wählt links oben den Controller aus, dessen Bezeichnung mit WindowsMR beginnt. Danach schaltet ihr den rechten Index Controller ein. Dieser sollte dann rechts oben erscheinen. Wählt ihn ebenfalls aus und legt den Index Controller an. Schiebt ihn so weit wie möglich nach hinten, damit ihr jetzt den rechten G2-Controller mit euren Finger fest packen könnt. Klickt außerdem auf "Copy Chaperone Bounds to profile".

Wählt danach rechts "very slow" aus und klickt auf "Start calibration".

Bevor ihr jedoch mit der Kalibrierung startet, erkläre ich euch noch, wie die Kalibrierung funktioniert. Hier wird nicht etwa der rechte G2-Controller mit dem rechten Index-Controller verschmolzen. Viel mehr wird die relative Position des WMR-Trackings an den Space-Calibrator weitergegeben, welche dann die relative Position des Lighthouse-Trackings ermitteln kann. Daher könntet ihr nun theoretisch auch den rechten G2-Controller und den linken Index-Controller in der Hand halten. Wichtig ist jedoch, dass die Controller selbst sich nicht in eurer Hand bewegen. Daher muss der Index-Controller fest sitzen und der G2-Controller fest in eurer Hand sein. Es ist egal, ob die Controller untereinander nah in der Hand liegen oder nicht, es ist ausschließlich wichtig, dass sie gleichzeitig und gleich bewegt werden.

Daher ist es auch wichtig, dass das Tracking der G2-Controller funktioniert. Dies erreicht ihr natürlich nur, wenn ihr den Controller vor eurer G2 bewegt und nicht das Tracking-Volumen verlasst. Wenn ihr die Kalibrierung startet, stellt einfach sicher, dass die Controller fest sitzen und ihr mit eurem Kopf die Controller so verfolgt, dass das Tracking funktioniert. Ihr könnt euch auch selbst im Raum bewegen, das ist alles egal. Wichtig ist nur, dass alles getrackt wird.

Die Kalibrierung könnte außerdem ebenfalls auf der Stufe "fast" vorgenommen werden, jedoch sind wir hier einfach mal penibel und möchten so viele Stichproben an Trackingdaten sammeln, wie wir können. Also nehmen wir uns die Zeit.

Sobald die Kalibrierung abgeschlossen ist, solltet ihr nun beide Controller so in eurer Hand sehen, wie sie in der Wirklichkeit auch in eurer Hand liegen.

Der Kalibrierungsvorgang ist nun abgeschlossen. Beendet SteamVR, schaltet alle Controller aus. Nehmt beide Index-Controller in die Hand und schaltet diese ein, während ihr im Cliffhouse seid. SteamVR öffnet sich von selbst und nach wenigen Sekunden solltet ihr eure Index Controller sehen. Spätestens jetzt habt ihr verstanden, dass das beidseitige Kalibrieren der Index-Controller ein Irrglaube ist.

Theoretisch wärt ihr jetzt schon fertig. Was jedoch noch fehlt, sind die Raumbegrenzungen. Wenn ihr es jetzt nämlich vorsichtig testet, werdet ihr merken, dass zwar das HMD auf die WMR-Raumbegrenzung anschlägt, aber leider nicht die Index-Controller. Das Ziel ist es nun, es genau umgekehrt zu machen: Wir brauchen keine HMD-Raumbegrenzung, sondern vor allem eine Controller-Raumbegrenzung für die Index-Controller.

Öffnet erneut den Space Calibrator und entfernt das Häkchen bei "Paste Chaperone bounds automatically".

Jetzt brauchen wir das zweite Tool: Die OVR Advanced Settings.

Öffnet dieses genau so wie den Space Calibrator aus dem SteamVR Dashboard unten links. Klickt links unten auf Settings, aktiviert dann "Allow External Edits" und "Force use SteamVR Chaperone Bounds (experimental)".

Jetzt beendet ihr SteamVR. Ab jetzt wird es bei jedem Start von SteamVR so sein, dass sich die SteamVR Raumvermessung startet. Das ist korrekt so. Später werden wir noch etwas konfigurieren, damit ihr diese nicht manuell schließen müsst. Zunächst brauchen wir die Raumvermessung jedoch. Daher startet nun SteamVR erneut.

Setzt die G2 ab und legt sie vorsichtig auf den Boden. Geht jetzt zum PC und folgt den Anweisungen der SteamVR Raumvermessung für Raumfüllendes VR.

Wenn ihr fertig seid, setzt die G2 wieder auf. Nun könnt ihr sehen, dass die Raumgrenzen angezeigt werden. Testes es vorsichtig aus! Damit die Einstellungen gespeichert werden, öffnet ihr erneut die OVR Advanced Settings, klickt links auf Chaperone und dann auf "new profile". Benennt dieses neue Profil bspw. mit G2 und klickt auf "save". Wenn ihr demnach irgendwann mal Probleme haben solltet, könnt ihr das Profil immer wieder neu laden.

An dieser Stelle der Hinweis: Das Lighthouse-Tracking und dessen Raumvermessung ist "für die Ewigkeit". D.h., egal was ihr mit eurer G2 anstellt, die Raumgrenzen des Lighthouse Trackings werden immer vorhanden sein. Achtet lediglich darauf, dass sich die Basisstationen nicht verschieben. Stellt daher sicher, dass diese fest an der Wand oder an der Decke angebracht sind, bevor ihr mit diesem Tutorial beginnt. Was sich jedoch mal verstellen kann, ist die Position der Controller selbst, also Drifting, wie zum Anfang des Videos erwähnt. Dazu später mehr.

Greift jetzt über das SteamVR Dashboard auf euren Desktop zu, öffnet das WMR-Portal und deaktiviert die "Darstellung der Raumgrenzen". Ab jetzt könnt ihr die G2 ohne Raumgrenzen bspw. sitzend in eurem Racing-Rig oder an eurem Schreibtisch mit euren G2-Controllern benutzen und separat dazu die Index Controller samt dessen Raumgrenzen.

Im großen und ganzen haben wir nun schon alles erledigt. Bevor ihr weitermacht, testet es etwas aus und bewertet für euch das Lighthouse-Tracking.

Hier noch kurz der Hinweis: Sollte es zu Drifting kommen, d.h. die Index Controller werden in VR an einer anderen Stelle dargestellt, als sie in Wirklichkeit gehalten werden, öffnet den Space Calibrator aus dem SteamVR Dashboard, wählt oben links die HP Reverb Virtual Reality Headset G20 aus und klickt rechts auf einen der beiden Index Controller.

Bei Calibration Speed stellt ihr "fast" ein. Legt jetzt eine Hand samt des Controllers auf euren Kopf, sodass es wie ein Einhorn aussieht. Ihr müsst einen sicheren Halt auf eurem Kopf haben. Es geht hier um die Index Controller, nicht um die G2 Controller.

Wenn ihr gleich euren Kopf bewegt, darf die Hand mit dem Controller nicht verrutschen, sondern muss sich parallel zum Kopf mitbewegen. Startet also jetzt die Kalibrierung und bewegt euren Kopf in einer 8er Bewegung umher. Die Kalibrierung auf fast funktioniert super schnell und die Index Controller sollten nun wieder an Ort und Stelle sein. Falls, warum auch immer, doch mal was schief gelaufen ist, wiederholt die Kalibrierung mit euren G2 Controllern, wie zuvor beschrieben. Lasst hier jedoch den Schritt "Copy Chaperone Bounds to profile" aus.

Außerdem wird sich die Bodenhöhe von Zeit zu Zeit ändern. Um dies zu beheben, klickt in den OVR Advanced Settings auf Space Fix. Legt dann einen Index Controller auf den Boden und klickt mit dem anderen auf „Fix Floor“. Danach ist die Bodenhöhe neu kalibriert. Das ist vor allem praktisch, da man auch während des Spielens die Bodenhöhe verstellen kann. Leider funktioniert dies jedoch wirklich nur mit den Index Controllern und nicht mit den G2 Controllern.

Das Problem an der Kombination aus den beiden Tracking-System ist jedoch, dass sie nicht nahtlos miteinander arbeiten. D.h. die Basisstationen gehen nicht automatisch in den Stand-By-Modus, wenn man SteamVR beendet und sie starten auch nicht, wenn man SteamVR startet. Außerdem ist das ständige Beenden der SteamVR Raumvermessung nervig und erfordert oft auch, dass man dies am PC selbst schließt, da es dafür keinen VR-Modus gibt.

Für diese Probleme gibt es abschließend eine Lösung: Den MixedVR Manager.

monstermac77 hat ein Skript und einen Dienst geschrieben, der auf eurem PC ausgeführt wird. Diesen habe ich etwas erweitert bzw. angepasst.

Dieser Dienst sorgt dafür, dass man die G2 mit den Index Controllern wie folgt benutzen kann:

G2 manuell per Funksteckdose einschalten und warten, bis sich das WMR-Portal öffnet,
Index Controller anlegen und die G2 aufsetzen,
Index Controller einschalten,
SteamVR wird jetzt automatisch durch das Einschalten der Index Controller gestartet, danach werden die
Lighthouse-Basisstationen automatisch gestartet und
die Raumvermessung wird automatisch beendet.

Wenn man mit VR aufhören will, beendet man SteamVR im Dashboard: Die Index Controller und die Lighthouse-Basisstationen werden ausgeschaltet und das WMR-Portal schließt sich. Danach kann die G2 per Funksteckdose ausgeschaltet werden.

Ursprünglich hat das Tool sogar eine Möglichkeit an Bord, die G2 automatisch im Geräte-Manager eures PCs zu aktivieren und zu deaktivieren, sodass das HP-Logo auch erlischt, obwohl sie sonst komplett verbunden ist. Ich habe es nun jedoch länger getestet und hatte damit mehr Probleme, als Erfolg. Daher habe ich es in meinem Fork des GitHub Downloads im Skript deaktiviert. Verwendet daher unbedingt die empfohlene Lösung über eine Funksteckdose.

Man muss jedoch beachten, dass jede Automation manchmal auch etwas macht, was man gerade eigentlich nicht will. Damit meine ich nicht, dass sie falsch funktioniert. Jedoch würden eben bei jedem SteamVR start, gleich aus welchem Grund SteamVR gestartet wurde, auch die Basisstationen usw. eingeschaltet werden. Das gleiche gilt natürlich auch für einen SteamVR Neustart, wo dann alles ausgeschaltet wird, und danach eingeschaltet wird.

Wer also häufig verschiedene Setups am gleichen PC verwendet, d.h. G2 mit G2 Controllern, G2 mit Index Controller, Oculus Quest 2 via Virtual Desktop usw., der sollte das Skript eher manuell als automatisch ausführen. Dazu später mehr.

Falls ihr jedoch kein Bluetooth in eurem PC verbaut habt, könnt ihr auch eine Android-App nutzen oder bspw. einen Laptop, der Bluetooth hat, parallel dazu benutzen. Natürlich könnt ihr die Stromzufuhr zu den Basisstationen auch manuell trennen und wiederherstellen. Auch hier empfehle ich dann jedoch Funksteckdosen. Falls ihr dies so betreiben wollt, muss das Skript angepasst werden. Schreibt mich dazu im Discord an.

Die folgenden Schritte beziehen sich demnach auf den Fakt, dass Bluetooth im VR-PC vorhanden ist.

Ich zeige euch jetzt die Möglichkeit, alles automatisiert zu konfigurieren. Danach zeige ich euch die erwähnte Möglichkeit, die Lighthouse-Stationen manuell über eine Batch-Datei einzuschalten.

Ladet die ZIP-Datei auf euren Desktop herunter und entpackt sie. Öffnet den entpackten Ordner und verschiebt den Ordner "vr-main" auf euer Laufwerk C. Öffnet den Ordner "vr-main", danach den Ordner "bin".

Danach öffnet ihr ein Eingabeaufforderungsfenster, kurz command prompt, indem ihr die Windowstaste+R drückt, im Ausführen-Fenster dann cmd eingebt.

Als erstes müsst ihr nun im Command Prompt in das Verzeichnis wechseln, in welchem ihr gleich die Befehle ausführen möchtet. Daher kopiert euch den Pfad des zuvor geöffneten Ordners in die Zwischenablage und gebt danach "cd" ein, danach ein Leerzeichen und dahinter fügt ihr den kopierten Pfad aus eurer Zwischenablage wieder ein.

Jetzt werden alle Befehle in diesem Verzeichnis ausgeführt. Ihr könnt nun die MAC-Adressen eurer Lighthouse-Basisstationen suchen. Dies macht ihr, indem ihr folgendes eingebt:
lighthouse-keeper.exe 2 discover

Die Zahl 2 steht für Basisstationen der Version 2.0. Wenn ihr Basisstationen der Version 1.0 habt, ersetzt die 2 durch eine 1.

Danach drückt auf Enter und wartet, bis das Tool mithilfe eures Bluetooths im PC die Basisstationen gefunden hat.

Wie ihr seht, muss ich den Befehl hier bei mir mehrmals ausführen. Das ist nicht schlimm. Wichtig ist, dass ihr am Ende so viele eindeutige MAC-Adressen gefunden habt, wie ihr Basisstationen verwendet.

Nun könnt ihr im Windows-Explorer wieder eine Ebene zurück gehen, um wieder im vr-main-Ordner zu landen. Dort macht ihr einen Rechtsklick auf "config.bat" und klickt auf Bearbeiten.

Hier ersetzt ihr die MAC-Adressen durch eure. Achtet ebenfalls darauf, auch hier die richtige Lighthouse-Basisstation-Version einzutragen.

Die restlichen Einstellungen können gleich bleiben, sofern der Steam- und SteamVR Installationspfad stimmt. Falls nicht, passt ihn hier an.

Schließt die config.bat und klickt auf Speichern.

Nun müsst ihr den mixedvr-manager-dienst in den Autostart legen. Das macht ihr, indem ihr die Windows+R Taste drückt, um Ausführen zu öffnen, um dort dann shell:startup eingeben zu können.

Der geöffnete Ordner enthält manuell hinzugefügte Autostartprogramme. Kopiert die mixedvr-manager-launcher.vbs, die sich im vr-main-Verzeichnis befindet, macht einen Rechtsklick im Autostart-Ordner und klickt auf Verknüpfung einfügen, nicht jedoch auf einfügen!

Nun startet ihr euren PC neu und bemerkt dann erstmal nichts.

Wenn ihr jetzt die G2 per Funksteckdose einschaltet, wartet, bis sich das WMR-Portal öffnet.

Geht zu eurem Playspace, setzt euch die G2 auf und legt die Index Controller an.

Schaltet beide Index Controller ein und beobachtet, dass sich SteamVR von selbst öffnet.

Das Tool überwacht nun im Hintergrund, ob sich SteamVR sowie die Raumvermessung öffnen. Die Raumvermessung wird nun automatisch geschlossen. Währenddessen sind auch eure Lighthouse-Basisstationen von selbst hochgefahren, falls sie nicht noch eingeschaltet waren.

Wenn ihr jetzt SteamVR ausschaltet, wird auch automatisch das WMR-Portal ausgeschaltet sowie die Basisstationen heruntergefahren. Probiert dies aus.

Normalerweise sollte alles funktionieren, daher führe ich hier im Video nicht alle potentiellen Fehlerquellen auf. Falls etwas nicht funktioniert, schreibt es gerne in die Kommentare oder besser noch: Kommt auf unseren Discord, damit ich euch helfen kann. 

Falls ihr die nicht automatisierte Methode bevorzugt, d.h. dass ihr selbst mit einem Skript die Basisstationen ein- und ausschalten wollt und die Raumvermessung selbst schließen wollt, ersetzt eure Lighthouse-MAC-Adressen in den Skripts "manual on" und "manual off" im Ordner "bin" und führt diese beiden Skripts dann bei Bedarf aus, um die Basisstationen ein- und auszuschalten. Hier könnt ihr euch Verknüpfungen auf eurem Desktop erstellen.

Falls ihr diesen manuellen Weg bevorzugt, entfernt jedoch die Verknüpfung im Autostart-Ordner. Ihr könnt natürlich auch die Datei mixedvr-manager-launcher.vbs manuell starten, damit die Überwachung des MixedVR-Managers erst dann beginnt, wenn ihr spielen möchtet. Beenden könnt ihr sie, indem ihr im Taskmanager unter Details den Prozess cmd beendet.

Jetzt sind wir am Ende des Tutorials angekommen. Ich bin mir sicher, dass dies auf den ersten Blick sehr kompliziert klingt. Letztlich ist es jedoch nicht die Vorgehensweise, die kompliziert ist, sondern bspw. die fehlende Übung mit Skripts. Ich selbst brauche für den ganzen Vorgang vom Beginn des Videos bis zum Ende ca. 15 Minuten.

Viele Schritte des Tutorials müssen auch mit nativen Lighthouse-VR-Headsets vorgenommen werden. Nur wenige Schritte sind wirklich wegen der Hybridlösung nötig. Schreckt also nicht vor der Vorgehensweise ab, sondern höchstens vom Preis der Anschaffung.

Ich persönlich habe folgendes bezahlt:

EUR 299,- für meine Index Controller
EUR 270,- für meine gebrauchten HTC Lighthouse 2.0 Basisstationen
EUR 40,- für meine beiden HTC Vive Tracker Dongles
EUR 534,- für meine HP Reverb G2
= EUR 1.143

Nicht vergessen darf man jedoch, dass ich wegen des Kaufs der Index Controller den Kaufpreis von Half-Life: Alyx im Nachhinein erstattet bekommen habe. Dies gilt auch heute noch. Daher sind es insgesamt rund EUR 1.100,- für die Hybridlösung.

Für mich also fast kostenneutral zu dem Valve Index Komplettset. Wenn man beachtet, dass die G2 auch ohne Lighthouse-Tracking betrieben werden kann und für mich eine bessere VR-Brille darstellt, vor allem in Sachen Bildqualität, ist diese Lösung ein echter Mehrwert.

Ich bin mir jedoch bewusst, dass nicht jeder diese Rechnung aufstellen kann, da die HP Reverb G2 regulär EUR 699,- kostet. Außerdem ist die Nichtverfügbarkeit der Dongles und oft auch der Index Controller ein Grund, von dieser Lösung Abstand zu nehmen.

Daher kann ich niemandem empfehlen, dieses Setup zu höheren Kosten zu kaufen. Es funktioniert zwar super und es gibt nichts besseres, aber meiner Meinung nach ist die G2 samt ihres Trackings und der Controller ihr Geld wert und es ist kein Upgrade nötig.

Für alle, die jedoch von der Valve Index kommen oder zuvor schon Lighthouse verwendet haben, für den kann dies eine gute Erweiterung darstellen.

Lest euch dieses Tutorial erneut durch oder schaut es euch als Video an, um alles in Ruhe zu verstehen.

ENDE: Bitte bewertet das oben verlinkte YouTube-Video, weshalb dieses schriftliche Tutorial erst entstanden ist, und lasst ein Abonnement da, wenn ihr zukünftig mehr über VR sehen möchtet. Eure Discord-Mitgliedschaften, eure Kommentare und eure Abos motivieren mich, auch zukünftig Content bereitszustellen.

Bis bald, euer Marco.
