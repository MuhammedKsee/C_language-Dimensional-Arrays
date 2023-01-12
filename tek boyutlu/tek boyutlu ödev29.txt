/*
Klavyeden girilen cumledeki en uzun ve en kisa kelime arasindaki
karakter sayisi farkini bulan program.
*/
#include <stdio.h>
#include <string.h>

int main(void) {
  char sentence[100];
  printf("Bir cumle girin: ");
  gets(sentence);

  int word_count = 0;
  for (int i = 0; i < strlen(sentence); i++) {
    if (sentence[i] == ' ') {
      word_count++;
    }
  }
  word_count++;
  char words[word_count][20];
  int word_index = 0;
  int char_index = 0;
  for (int i = 0; i < strlen(sentence); i++) {
    if (sentence[i] != ' ') {
      words[word_index][char_index] = sentence[i];
      char_index++;
    } else {
      words[word_index][char_index] = '\0';
      word_index++;
      char_index = 0;
    }
  }
  words[word_index][char_index] = '\0';
  int longest_index = 0;
  int shortest_index = 0;
  for (int i = 0; i < word_count; i++) {
    if (strlen(words[i]) > strlen(words[longest_index])) {
      longest_index = i;
    }
    if (strlen(words[i]) < strlen(words[shortest_index])) {
      shortest_index = i;
    }
  }


  int diff = strlen(words[longest_index]) - strlen(words[shortest_index]);
  printf("En uzun ve en kisa kelimeler arasindaki karakter sayisi farki: %d\n", diff);

  return 0;
}
