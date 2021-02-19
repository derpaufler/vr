English-Tutorial at the bottom of the page (work in progress).

Dieses Tutorial ist eine Übersetzung und Anpassung der Tutorials von PumkinSpice und monstermac77:
This Tutorial is a translation and modified version of the tutorials of PumkinSpice and monstermac77:
https://github.com/PumkinSpice/MixedVR/wiki/ReadMe
https://github.com/monstermac77/vr

Mit Zustimmung von monstermac77 fasse ich alle Schritte auf Deutsch zusammen und stelle euch im Laufe des Tutorials eine Anpassung seines Tools "MixedVR Manager" bereit.
With the approval of monstermac77 I sum up every step in German and I present you a modified version of his tool "MixedVR Manager".

======

Deutsches/German Tutorial:

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

===============================================

English/englisches Tutorial (work in progress/in Arbeit):

In this tutorial I show you how you can pair the HP Reverb G2 with the Index Controllers.

I will show you that it is very easy to implement if you follow this video tutorial. It is of course important that you don't skip a single step and really do everything exactly as I show and describe it to you. Skipping steps because you think you have done this and that beforehand, or you consider something as unnecessary, may lead to problems later on.

Once you've set it up, you don't need to do anything afterwards. If you ask yourself right at the beginning of the video that the index controllers will eventually drift away because the coordinates of the HP Reverb G2 change from time to time, then I'll also show you how quickly and easily you can fix this again. And this without a G2 controller to recalibrate.

My personal goal was to completely replace the HP Reverb G2 controllers. Not because I would find the tracking or the controllers themselves so bad, no, on the contrary, but the index controllers are simply much better. This also applies to me in comparison to the Oculus Touch controllers.

It was also a condition that I could use the HP Reverb G2 again at any time without the lighthouse tracking, e.g. again normally with the G2 controllers, without having to configure much. Since I have two playspaces, that's important to me.

Furthermore, the HP Reverb G2 with its combinable tracking systems turns out to be a real all-rounder, since with Lighthouse HMDs you always need the base stations, and that is really very cumbersome. Of course, the G2 won't be as portable as a Quest 2, and certainly not wireless, but this solution is really interesting for various playspaces.

All of this has only been made possible by the really dedicated tinkerers on Reddit. Visit in case of additional questions not only our Discord, but also the subreddit MixedVR.

Many thanks at this point, especially to the users monstermac77, pushrax, PumpkinSpice, Tetracyclic and the programmers of the OVR Advanced Settings. Above all, monstermac77 discussed one or the other thing with me personally, which is why I am able to introduce you to a really cool tool in the course of the video.

Now enough of the foreword! Let's get into the tutorial.

As a prerequisite, of course, you need the HP Reverb G2, the Index Controller and at least two Lighthouse Base Stations of version 1.0 or 2.0. Whether these are from Valve or HTC is not relevant. What is not so obvious is the fact that you need a Bluetooth Low Energy dongle for each of the two index controllers. Unfortunately, you can't just use any dongle, you need either two official HTC Vive Tracker dongles or two Steam Controller dongles. Unfortunately, both are not readily available at the moment. Check back often at TundraLabs or on eBay.

You can of course also buy the HTC Vive tracker, as the dongles are already included, but they cost around EUR 160 each, and you cannot connect the trackers to the index controllers in parallel to the dongles. Therefore, I would advise against buying the trackers just because of the dongles.

If you want to use two Steam Controller dongles, you have to flash them. After that, they are no longer compatible with the Steam Controller. You can find the instructions for this in the video description, but I have not tested this myself and can therefore not help.

It is recommended to use the Vive Tracker Dongles in USB 2.0 ports, as USB 3.2 ports can cause interference with the radio signal. It is therefore essential that you use one USB 2.0 extension per dongle so that they are as close as possible to you and as far away from each other as possible.

For the best comfort, your PC itself needs at least Bluetooth 4.0 with sufficient range to reach the Lighthouse base stations. Small Bluetooth dongles in particular often have to struggle with range. However, if you don't have Bluetooth, you don't necessarily need to buy a dongle. More on that later.

All links to the sources and to things that you need or need to buy can be found in the video description.

In addition to the hardware, we also need a lot of software. The G2 must of course already be configured and set up. In addition, Steam and SteamVR must be installed, including of course the Windows Mixed Reality for SteamVR driver. Furthermore, the following free software must be downloaded and installed immediately afterwards: The OVR Advanced Settings from the Steam Store and the OpenVR SpaceCalibrator from GitHub.

So let's start with the setup.

First pull the power plug of the G2 out of the socket so that it doesn't switch on all the time when we don't need it. Before doing this, close the WMR portal, if it is open, so that the G2 is switched off properly. Incidentally, I can recommend a smart home plug or a radio-controlled socket here. This is the best and most reliable method to ensure that the G2 does not throw any errors and is only switched on when we need it.

Then you plug one of the two dongles together with the recommended USB extension into your PC. This should then be recognized by Windows. Wait until it is "set up and ready to use".

Open Steam and SteamVR. It is true that no VR headset is connected. In SteamVR click on Settings, Devices, Pair controllers on the desktop. Select the Valve Index Controller and follow the on-screen instructions to pair one of the two controllers. As soon as the controller is coupled, confirm the coupling with "OK" and switch off the index controller. Then pull the dongle off the PC. Incidentally, it is not relevant in which port you later plug the dongles back in, as long as it is always the recommended USB 2.0 port.

Then repeat the whole thing again with the second dongle and the second controller.

When the pairing is complete, confirm the process with "OK" and switch off the index controller. You can now plug in the first dongle again and then switch on both controllers. Both controllers should now appear as connected. If you have already pointed Lighthouse base stations at you and they are switched on, these will also be displayed.

Otherwise you can do that now. Switches on the Lighthouse base stations. If they are in sleep mode, disconnect the power for a few seconds and reconnect them.

It is also important here: the Lighthouse base stations must already be installed. Moving it later ensures that most of the steps were in vain and have to be repeated.

All Lighthouse devices are now displayed and are successfully connected.

By the way: If the controllers need a firmware update, please do so. It is not recommended for base stations with version 1.0, but not with 2.0 devices. I cannot say why that is so. However, if everything works in the end even without a firmware update, you can save yourself the update anyway. Never change a running system.

Now you switch off the index controller, but leave everything plugged in and the base stations switched on.

Still on the desktop, in SteamVR go to Settings, Start / Exit and then to "Select overlay applications at startup". Switches "Space Calibrator" and "OVR Advanced Settings" to "On" and everything else, especially fpsVR, to "Off". At the very end you can turn on your personal overlay applications such as fpsVR, which you may have turned off now. Also enables the option under Controller in the settings that the index controllers are automatically switched off when SteamVR is closed.

Now quit SteamVR.

Now switch your HP Reverb G2 back on and wait until the WMR portal has opened.

In the WMR portal you have to switch on the room limitation and set it up. You do this now even if you have already set it up. It is very important that you do this carefully so that you can later check that everything is working well. Also provides subsequently ensure that your true ground level. Pro tip here: Place a controller on the floor and look at the controller when you adjust the height. If the controller is covered by the floor, you know how to adjust the floor height.

Open SteamVR from the Cliffhouse and carefully test whether your room limitation works. This must be triggered by both the HMD and the controller. If you see the limit of the room and everything is in order, the establishment has been successful. Now put the Steam Controller in front of you on the floor. Put the left G2 controller aside and switch it off beforehand by holding down the Windows button.

Open the SteamVR dashboard, click on the three dots in the lower left and open Space Calibrator. In the top left, select the controller whose name begins with WindowsMR. Then you switch on the right index controller. This should then appear at the top right. Select it too and create the index controller. Push it back as far as possible so that you can now grasp the right G2 controller with your fingers. Also click on "Copy Chaperone Bounds to profile".

Then select "very slow" on the right and click on "Start calibration".

But before you start with the calibration, I'll explain how the calibration works. The right G2 controller is not merged with the right index controller here. Rather, the relative position of the WMR tracking is passed on to the space calibrator, which can then determine the relative position of the lighthouse tracking. So you could theoretically hold the right G2 controller and the left index controller in your hand. It is important, however, that the controllers themselves do not move in your hand. Therefore the index controller has to be firmly seated and the G2 controller has to be firmly in your hand. It doesn't matter whether the controllers are close together or not, it is only important that they are moved simultaneously and equally.

Therefore it is also important that the tracking of the G2 controllers works. Of course , you can only achieve this if you move the controller in front of your G2 and do not leave the tracking volume. When you start the calibration, just make sure that the controllers are tight and that you are following the controllers with your head so that the tracking works. You can also move yourself in space, it doesn't matter. The only important thing is that everything is tracked.

The calibration could also be carried out at the "fast" level, but we are just being meticulous here and want to collect as many samples of tracking data as we can. So let's take our time.

As soon as the calibration is completed, you should now see

both controllers in your hand as they are in your hand in reality.

The calibration process is now complete. Quits SteamVR, turns off all controllers

. Take both index controllers in hand and switch them on while you are in the Cliffhouse

. SteamVR will open by itself and after a few seconds you should see your index

controller. By now you have understood that calibrating the index controller

on both sides is a mistake.

In theory, you'd be done by now. What is still missing, however, are the room boundaries.

If you test it carefully now, you will notice that the HMD hits the

WMR room delimitation, but unfortunately not the index controller. The goal is

now to do it the other way around: We don't need an HMD room delimitation, but above all

a controller room delimitation for the index controller.

Open the Space Calibrator again and uncheck "Paste Chaperone bounds automatically".

Now we need the second tool: The OVR Advanced Settings.

Open this just like the Space Calibrator from the SteamVR dashboard at the bottom left. Click

on Settings at the bottom left, then activate "Allow External Edits" and "Force use SteamVR Chaperone

Bounds (experimental)".

Now you quit SteamVR. From now on, every

time SteamVR is started, the SteamVR room survey will start. That is correct. Later we will configure something

so that you don't have to close it manually. First, however, we need

the room measurement. Therefore, SteamVR starts again.

Put the G2 down and carefully place it on the floor. Now go to the PC and follow the

instructions of the SteamVR room measurement for room-filling VR.

When you're done, put the G2 back on. Now you can see that the room boundaries

are displayed. Test it out carefully! To save the settings,

open the OVR Advanced Settings again, click on Chaperone on the left and then on "new

profile". Name this new profile, for example, G2 and click on "save". If

you should have problems at any time, you can always reload the profile.

At this point the note: The lighthouse tracking and its room measurement is "for eternity".

That means, no matter what you do with your G2, the spatial limits of the lighthouse tracking will

always be present. Just make sure that the base stations do not move.

So make sure they are securely attached to the wall or ceiling before

starting this tutorial. What can change, however, is the position of

the controller itself, i.e. drifting, as mentioned at the beginning of the video.

More on that later .

Now access your desktop via the SteamVR dashboard, open the WMR portal and

deactivate the "display of room boundaries". From now on you can use the G2 without room boundaries, e.g.

sitting in your racing rig or at your desk with your G2 controllers

and separately the index controller and its room boundaries.

By and large, we've already done everything. Before you continue, test

it out a little and evaluate the lighthouse tracking for you.

Here is a brief hint: Should drifting occur, i.e. the index controllers are displayed in

a different position in VR than they are actually held, open

the Space Calibrator from the SteamVR dashboard, select the HP Reverb Virtual Reality

Headset at the top left G20 and right-click on one of the two index controllers.

At Calibration Speed you set "almost". Now put one hand including the controller

on your head so that it looks like a unicorn. You have to have a secure hold on

your head. This is about the index controller, not the G2 controller.

If you move your head right away, the hand with the controller must not slip,

but must move parallel to the head. So now start the calibration and move

your head around in a figure of eight. The calibration to almost works super fast

and the index controllers should now be back in place. If, for whatever

reason , something went wrong, repeat the calibration with your G2 controllers

as described above. However, leave out the "Copy Chaperone Bounds to profile" step here

.

Also, the height of the ground will change from time to time. To fix this, click

Space Fix in the OVR Advanced Settings. Then place an index controller on the floor

and click with the other on "Fix Floor". The floor height is then recalibrated.

This is especially useful because you can adjust the floor height while playing.

Unfortunately this only works with the Index Controllers and not with the

G2 Controllers.

The problem with the combination of the two tracking systems, however, is that they don't work

seamlessly with each other. This means that the base stations do not automatically go into stand-by mode

when you exit SteamVR and they do not start when you start SteamVR. In addition

, the constant termination of the SteamVR room measurement is annoying and often requires that you

close it yourself on the PC, as there is no VR mode for it.

Finally, there is a solution to these problems: The MixedVR Manager.

monstermac77 wrote a script and a service that runs on your PC

. I have expanded or adapted this a little.

This service ensures that you can use the G2 with the Index Controllers as follows

:

Switch on the G2 manually via a radio-controlled socket and wait until the WMR portal opens,

create the Index Controller and put on the G2, switch on the Index Controller,

SteamVR is now automatic started by switching on the index controller, then

the Lighthouse base stations are started automatically

and the room measurement is ended automatically.

If you want to stop VR, you quit SteamVR in the dashboard: The index controller

and the Lighthouse base stations are switched off and the WMR portal closes. The G2 can

then be switched off via a radio-controlled socket.

Originally, the tool even had the option of automatically activating and deactivating

the G2 in the device manager of your PC, so that the HP logo disappears even though it is

otherwise completely connected. However, I have now tested it longer and had

more problems with it than it was successful. So I disabled it in my GitHub download fork in the

script. It is therefore essential to use the recommended solution via a radio-controlled socket.

However, you have to note that every automation sometimes does something that you

don't actually want. I don't mean that it works wrong. However,

with every SteamVR start, for whatever reason SteamVR was started, the base stations

etc. would also be switched on. The same applies, of course, to a SteamVR restart,

where everything is switched off and then switched on.

So if you often use different setups on the same PC, ie G2 with G2 controllers,

G2 with index controller, Oculus Quest 2 via Virtual Desktop, etc., you should run the script

manually rather than automatically. More on that later.

However, if you don't have Bluetooth built into your PC, you can also use an Android app

or, for example, use a laptop that has Bluetooth in parallel. Of course, you can

also manually disconnect and restore the power supply to the base stations.

Here, too, I recommend radio-controlled sockets. If you want to do this, the

script has to be adapted. Write to me about this in the Discord.

The following steps therefore relate to the fact that Bluetooth is present in the VR PC

.

I will now show you the possibility to configure everything automatically. Then

I'll show you the mentioned option of switching the Lighthouse stations on manually via a batch file.

Download the ZIP file to your desktop and unzip it. Open the unzipped folder

and move the folder "vr-main" to your drive C. Open the folder "vr-main",

then the folder "bin".

Then you open a command prompt window, short command prompt, by pressing the Windows

key + R , then enter cmd in the run window.

First you have to switch to the directory in the command prompt in which you

want to execute the commands. Therefore, copy the path of the previously opened

folder to the clipboard and then enter "cd", then a space and then

paste the copied path from your clipboard again.

Now all commands in this directory will be executed. You can now search for

the MAC addresses of your Lighthouse base stations. You do this by entering the following: lighthouse-keeper.exe

2 discover

The number 2 stands for base stations of version 2.0. If you have version 1.0 base stations

, replace the 2 with a 1.

Then press Enter and wait until the tool has found the base stations in the PC using your Bluetooth

.

As you can see, I have to carry out the order here several times. That's not bad.

It is important that you have found as many unique MAC addresses as you use base stations

.

Now you can go back one level in Windows Explorer to land

back in the vr-main folder . There you do a right click on "config.bat" and click on edit.

Here you replace the MAC addresses with yours. Also make sure that you enter the correct

Lighthouse base station version here as well .

The remaining settings can remain the same as long as the Steam and SteamVR installation path

is correct. If not, adjust it here.

Close the config.bat and click on save.

Now you have to put the mixedvr manager service into the autostart. You do this by

pressing the Windows + R key to open Run and then enter shell: startup

.

The opened folder contains manually added startup programs. Copy the mixedvr-manager-launcher.vbs that

is in the vr-main directory, right-click in the startup folder

and click on paste shortcut, but not on paste!

Now you restart your PC and don't notice anything at first.

If you now switch on the G2 via a radio-controlled socket, wait until the WMR portal opens.

Go to your playspace, put on the G2 and put on the index controller.

Turns on both Index Controllers and observes that SteamVR opens by itself.

The tool now monitors in the background whether SteamVR and the room measurement open.

The room measurement is now closed automatically. In the meantime, your Lighthouse base stations will

also start up automatically if they were not switched on.

If you turn off SteamVR now, the WMR portal will also be automatically turned off and

the base stations shut down. Try this out.

Normally everything should work, so I'm not listing all potential sources of error

here in the video . If something doesn't work, please write it in the

comments or better still: Come to our Discord so I can help you.

If you prefer the non-automated method, ie you want to switch the base stations on and off

yourself with a script and want to close the room measurement yourself

, replace your Lighthouse MAC addresses in the scripts "manual on" and "manual off"

in the folder "bin" and then runs these two scripts as needed to turn the base stations

on and off. Here you can create shortcuts on your desktop.

If you prefer this manual way, remove the link in the startup folder.

You can of course also start the file mixedvr-manager-launcher.vbs manually so that the monitoring of the

MixedVR manager only starts when you want to play. You can end it

by closing the cmd process in the task manager under details.

We have now come to the end of the tutorial. I'm sure this sounds very complicated at first

glance. Ultimately, however, it is not the procedure that is complicated

, but, for example, the lack of practice with scripts. I myself need about 15 minutes

for the whole process from the beginning of the video to the end.

Many steps of the tutorial also need to be done with native Lighthouse VR headsets

. Only a few steps are really necessary because of the hybrid solution. So

don't put off the approach, but rather the price of the purchase.

I personally paid the following:

EUR 299.00 for my Index Controller EUR 270.00 for my used HTC Lighthouse

2.0 base stations EUR 40.00 for my two HTC Vive Tracker

Dongles EUR 534.00 for my HP Reverb G2

= EUR 1,143

Don't forget However, it is safe to say that I got the purchase price of Half-Life: Alyx reimbursed

after the purchase of the Index Controller . This is still true today.

Therefore it is a total of around EUR 1,100 for the hybrid solution.

For me, almost no cost to the Valve Index complete set. If you consider that

the G2 can also be operated without lighthouse tracking and that it represents better VR glasses for me

, especially in terms of image quality, this solution is a real added value.

I am aware, however, that not everyone can issue this invoice, as the HP

Reverb G2 normally costs EUR 699.00. In addition, the unavailability of the dongles and

often the index controller is a reason to refrain from this solution.

Therefore, I cannot recommend anyone to buy this setup at a higher cost. It works

great and there is nothing better, but in my opinion the G2, including its

tracking and controller, is worth the money and no upgrade is necessary.

However, for everyone who comes from Valve Index or has used Lighthouse before

, this can be a good addition.

Watch this video again to understand everything in peace the second time you watch it.

Use the timestamps for orientation and also like to use my written instructions.

This is linked in the video description.

Thank you for watching. Please rate this video and leave a subscription

if you want to see more about VR in the future. Your Discord memberships, your comments

and your subscriptions motivate me to continue providing content in the future. See you soon, your Marco.
