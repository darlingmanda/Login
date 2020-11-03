# Login
teste
lass Passaro                       // classe base
{
public:
   virtual void MostraNome()
   {
      std::cout << "um passaro";
   }
   virtual ~Passaro() {}
};

class Cisne: public Passaro         // Cisne é um pássaro
{
public:
   void MostraNome()
   {
      std::cout << "um cisne";        // sobrecarrega a função virtual
   }
};

int main()
{
   Passaro* passaro = new Cisne;

   passaro->MostraNome();            // produz na saída "um cisne", e não "um pássaro"

   delete passaro;
}

