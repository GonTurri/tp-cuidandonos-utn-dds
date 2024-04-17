```java
Class Viaje{
  private CalculadorDemora calculadorDemora;
  private Ubicacion puntoPartida;
  private Ubicacion destino;
  private List<Parada> paradas;
  private boolean avisaPorParada;


  private Integer getDemoraAproximada(){
    Integer total =0;
    if(paradas.isEmptpy()) return calculadorDemora.calcularDemora(puntoPartida,destino);
      total += calculadorDemora.calcularDemora(puntoPartida,paradas.get(0))
      for(Int i =1; i< paradas.size(); i++){
        total += calculadorDemora.calcularDemora(paradas.get(i-1),paradas.get(i));
      }
     total += calculadorDemora.calcularDemora(paradas.get(paradas.size()-1),destino);
     if(!avisaParada) total += paradas.stream().mapToInt(p -> p.getTiempoEspera()).sum();
     return total;
  }
    
  
}
```
