DesarrolloPreguntas.R
#EJERCICIO 1 #

ejemplos=sample(c("Positivo","Negativo","Neutros"),100,replace=TRUE)

n_positivos<-0
for (i in 1:length(ejemplos)){
  if("Positivo"==ejemplos[i]){n_positivos<-n_positivos+1}
}

n_negativos<-0
for (i in 1:length(ejemplos)){
  if("Negativo"==ejemplos[i]){n_negativos<-n_negativos+1}
}

n_neutros<-0
for (i in 1:length(ejemplos)){
  if("Neutros"==ejemplos[i]){n_neutros<-n_neutros+1}
}


#EJERCICIO 2 #

set.seed(10)
ejemplos=sample(c("Positivo","Negativo","Neutros"),10,replace=TRUE)


#EJERCICIO 3 #

set.seed(66)
Ejemplos=sample(c("Positivo","Negativo","Neutros"),10,replace=TRUE)

# EJERCICIO 4 #

cartas_sacadas=sample(c("A",2:10,"J","Q","K"),31,replace=TRUE)
set.seed(31)
Cuenta<-0
for (i in 1:length(Cartas_Sacadas)){
  if(Cartas_Sacadas[i]==2|Cartas_Sacadas[i]==3|Cartas_Sacadas[i]==4|Cartas_Sacadas[i]==5|Cartas_Sacadas[i]==6) {
    Cuenta<-Cuenta+1 } else if (Cartas_Sacadas[i]=="A"|Cartas_Sacadas[i]=="J"|Cartas_Sacadas[i]=="Q"|Cartas_Sacadas[i]=="K"|Cartas_Sacadas[i]==10){
      Cuenta<-Cuenta-1} else if (Cartas_Sacadas[i]==7|Cartas_Sacadas[i]==8|Cartas_Sacadas[i]==9){
        Cuenta<-Cuenta+0
      }
      
mas1<-c(2:6)
menos1<-c("A","J","Q","K",10)
neutros<-c(7:9)
cuenta2<-0
variable<-mas1
for (i in 1:length(Cartas_Sacadas)){ for (n in 1:length(variable)){
  if(Cartas_Sacadas[i]==mas1[n]){cuenta2<-cuenta2+1}}
  variable<-menos1
  for(n in 1:length(variable)){
    if(Cartas_Sacadas[i]==menos1[n]){cuenta2<-cuenta2-1}
  }
}
