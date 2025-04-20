# WpfDataBinding

esempio pratico di data binding bidirezionale (two-way) in WPF (Windows Presentation Foundation) usando MVVM semplificato, con INotifyPropertyChanged per notificare le modifiche alle proprietà.

1) INotifyPropertyChanged :  interfaccia che serve a notificare alla UI che una proprietà è cambiata → fondamentale per il data binding dinamico.
   
2) BoundText : proprietà bindata

3) OnpropertyChange : metodo che usa un attributo speciale ([CallerMemberName]) che viene usato per ottenere automaticamente il nome del metodo o della proprietà chiamante, senza doverlo specificare manualmente come stringa.
   
4) XAML -> TextBox : Binding su BoundText con proprietà bind

                 Mode="OneWayToSource" → il testo scritto nella TextBox aggiorna BoundText, ma non viceversa.

                 UpdateSourceTrigger=PropertyChanged → aggiorna BoundText ad ogni carattere digitato, non solo quando la TextBox perde il focus
