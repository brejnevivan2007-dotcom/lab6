#include <iostream>
#include <string>

using namespace std;

int main() {

    string $;

    cout << "napishi stroku";

    getline(cin, $);

    cout << "nashli chisla:" << endl;


    for (int i = 0; i < $.length(); i++) {
        
        if (isdigit($[i]) ||
            (($[i] == '+' || $[i] == '-') && i + 1 < $.length() && isdigit($[i + 1]))) {

            int go = i;


            while (i < $.length() && ((isdigit($[i]))||(i == go && ($[i] == '+'||$[i] == '-')))) {
                i++;
            }


            string № = $.substr(go, i - go);

            cout << № << endl;

            i--;
        }
    }
    return 0;
}
