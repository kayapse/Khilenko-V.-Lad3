# Khilenko-V.-Lad3
https://docs.google.com/document/d/1ex8yTQ-HDMdzWSaYX3p_eJeFN1j1jfhCG-osC1GKKPE/edit?tab=t.0

#include <iostream>
using namespace std;
int main() {
    auto isPrime = [](int num) -> bool { //// Якщо число менше або дорівнює 1, то воно не є простим
        if (num <= 1) {
            return false;
        }
        int i = 2; //перевірка з числа 2
        while (i * i <= num) {
            if (num % i == 0) {// Якщо num ділиться на i без залишку, то num не просте
                return false;
            }
            ++i; //перехід до наступного числа
        }
        return true; // Якщо нема дільників, то число просте
    };
    int n;//  для збереження введеного числа
    cout<<"Введіть число n: ";
    cin>>n;
    int current = 2;
    cout<<"Прості числа в діапазоні від 2 до " <<n<< ":\n";
    while (current <= n) {
        if (isPrime(current)) {
            cout<< current<<" ";
        }
        ++current; //перехід жо наступного числа
    }
    cout<<endl;
    return 0;
