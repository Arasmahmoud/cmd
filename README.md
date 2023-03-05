#atbash

#include <iostream>

using namespace std;

int main()
{
    char c,d;
    char plain_alphabet[26];
    char cipher_alphabet[26];
    for(int i=0;i<26;i++)
    {
        c='a'+i;
        plain_alphabet[i]=c;
        d='z'-i;
        cipher_alphabet[i]=d;
    }

    char plain[6]={'h','e','l','p','m','e'};
    char cipher[6];
    for(int k=0;k<6;k++)
    {
        for(int i=0;i<26;i++)
        {
            if(plain[k]==plain_alphabet[i])
            {
                cipher[k]=cipher_alphabet[i];
            }
        }
    }

    for(int k=0;k<6;k++)
    {
        cout<<cipher[k];
    }

    return 0;
}
-----------------------------------
#sezer

#include <iostream>

using namespace std;

int main()
{
   char plainText[4]={'T','E','S','T'};
   char cipherText[4];

   for(int i=0;i<4;i++)
   {
       plainText[i] = plainText[i]+3;
        if(plainText[i]>=90)
         {
           plainText[i]=plainText[i]-26;
         }
       cipherText[i]=plainText[i];
   }

    for(int i=0 ;i<4 ;i++ )
    {
        cout<<cipherText[i];

    }
    return 0;
}

--------------------------------------
#shift

#include <iostream>

using namespace std;

int main()
{
   char plainText[4]={'T','E','S','T'};
   char cipherText[4];
   int shift = 5;
   for(int i=0;i<4;i++)
   {
       plainText[i] = plainText[i]+shift;
        if(plainText[i]>=90)
         {
           plainText[i]=plainText[i]-26;
         }
       cipherText[i]=plainText[i];
   }

    for(int i=0 ;i<4 ;i++ )
    {
        cout<<cipherText[i];

    }
    return 0;
}

----------------------------------
#mult shift

#include <iostream>

using namespace std;
char shiftX(char c, int a);
int main()
{
   char plainText[14]={'A','L','A','N','A','N','D','S','H','E','N','Y','A','R'};
   int key[4]={1,3,2,5};
   char cipherText[14];
   int j=0;
   for(int i=0;i<14;i++)
   {
       cipherText[i]=shiftX(plainText[i],key[j]);
       if(j<3)#include <iostream>

using namespace std;

int main()
{
   char plainText[4]={'T','E','S','T'};
   char cipherText[4];
   int shift = 5;
   for(int i=0;i<4;i++)
   {
       plainText[i] = plainText[i]+shift;
        if(plainText[i]>=90)
         {
           plainText[i]=plainText[i]-26;
         }
       cipherText[i]=plainText[i];
   }

    for(int i=0 ;i<4 ;i++ )
    {
        cout<<cipherText[i];

    }
    return 0;
}
       {
           j++;
       }
       else
       {
           j=0;
       }
   }

    for(int i=0 ;i<14 ;i++ )
    {
        cout<<cipherText[i];

    }
    return 0;
}

char shiftX(char c, int a)
{
    c=c+a;
    if(c>=90)
        c=c-26;
    return c;
}
---------------------------------------
#polybuis

#include <iostream>

using namespace std;

int main()
{
    char plain[10] = {'d','e','f','e','n','d','w','a','l','l'};

    char poly[5][5] ={{'a','b','c','d','e'},
                      {'f','g','h','i','j'},
                      {'k','l','m','n','o'},
                      {'p','q','r','s','t'},
                      {'u','v','w','x','y'}};


    for(int k=0;k<10;k++)
    {
      for(int i=0;i<5;i++)
    {
        for(int j=0;j<5;j++)
        {
          if (plain[k] == poly[i][j])
          {
              cout<<i+1<<j+1<<" ";
          }
        }
    }
    }
    cout<<"\n"<<"================================"<<"\n";
    int row,col;
    int cipher[20]={1,4,1,5,2,1,1,5,3,4,1,4,5,3,1,1,3,2,3,2};
     for(int i=0;i<20;i+=2)
     {
         row=cipher[i]-1;
         col=cipher[i+1]-1;
         cout<<poly[row][col];
     }
return 0;
}
