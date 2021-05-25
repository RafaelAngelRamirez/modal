# Modal

Modal limpio y sencillo para Angular. 

>Requiere los estilos de bootstrap 4 o 5 para funcionar y para los iconos
>utiliza fontawesome

### Instalación

>`npm i @codice-progressio/modal`


### Uso

Agrega el modal en el modulo más alto que lo necesites. 

 
``` javascript
@NgModule({
  declarations: [AppComponent],
  imports: [BrowserModule, FormsModule, ModalModule],
  providers: [],
  bootstrap: [AppComponent],
})
export class AppModule {}

```

Llama al componente desde donde quieras definiendo su id. 

```html 

<codice-modal [id]="'unId'" (cerrado)="modalCerrado()">
  <h1>Funciona!</h1>
</codice-modal>


```

Para llamarlo solo inyecta el servicio `ModalService` en tu componente. 

```javascript 

idIdDelModal:string ="esteIdNoSeDebeRepetir"
constructor(private modalService: ModalService ){}

```

Y ejecuta `modalService.open(elIdDelModal)`.


Para cerrarlo ejecuta `modalService.close(idIdDelModal)`


