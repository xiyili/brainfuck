#include <stdio.h>

int main(){
  char memory[32768];
  char* pm = memory;
  char code[32768];
  scanf("%s", code);
  int fl = -1;
  int fld[32768];
  int l = 1;
  int lw;
  for (int i = 0; code[i] != 0; i++){
    if (code[i] == '+' && l == 1){
      (*pm)++;
    }else if (code[i] == '-' && l == 1){
      (*pm)--;
    }else if (code[i] == '>' && l == 1){
      pm++;
    }else if (code[i] == '<' && l == 1){
      pm--;
    }else if (code[i] == '['){
      fl++;
      fld[fl] = i;
      if (*pm == 0 && l == 1){
        l = 0;
        lw = fl;
      }
    }else if (code[i] == ']'){
      if (*pm != 0){
        i = fld[fl] - 1;
      } else if (fl == lw){
        l = 1;
      }
      fl--;
    } else if (code[i] == ','){
      *pm = getchar();
    } else if (code[i] == '.'){
      putchar(*pm);
    }
  }
}
