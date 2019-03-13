# exame

hi

disculpe la tardanza pero mi papa agarro la compu toda la noche por que tenia que pasar notas 

using figure;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace figure
{
    class hope
    {
        public string NombreFig { get; set; }

        public double BaseTriang { get; set; }
        public double AlturaTriang { get; set; }
        public double AreaTriang { get; set; }
        ///
        public double BaseRec { get; set; }
        public double AlturaRec { get; set; }
        public double AreaRec { get; set; }
        ///
        public double RadioCir { get; set; }
        public double AreaCir { get; set; }

        public virtual void Dathope()
        {
            Console.WriteLine("Mostrando los datos de las figuras");
        }
    }

    class Triangulo : hope
    {
        public override void Dathope()
        {
            Console.WriteLine("Ingrese el nombre de la figura deseada");
            base.NombreFig = Console.ReadLine();
            Console.WriteLine("Ingrese en los valores de la base:");
            base.BaseTriang = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Ingrese en los valores de la Altura:");
            base.AlturaTriang = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Ingrese en los valores del area:");
            base.AreaTriang = Convert.ToInt32(Console.ReadLine());
        }
    }
    class Rectangulo : hope 
    {
        public override void Dathope()
        {
            Console.WriteLine("Ingrese el nombre de la figura deseada");
            base.NombreFig = Console.ReadLine();
            Console.WriteLine("Ingrese en los valores de la base:");
            base.BaseRec = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Ingrese en los valores de la Altura:");
            base.AlturaRec = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Ingrese en los valores del area:");
            base.AreaRec = Convert.ToInt32(Console.ReadLine());
        }
    }
    class Circulo : hope
    {
        public override void Dathope()
        {
            Console.WriteLine("Ingrese el nombre de la figura deseada");
            base.NombreFig = Console.ReadLine();
            Console.WriteLine("Ingrese en los valores del radio:");
            base.RadioCir = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Ingrese en los valores del area:");
            base.AreaCir = Convert.ToInt16(Console.ReadLine());
        }
    }
}


    class figuras 
    {
        static void Main(string[] args)
        {

            var trian = new Triangulo();
            trian.Dathope();
            Console.WriteLine("El nombre de la figura es:{0}", trian.NombreFig);
            Console.WriteLine("El tamaño de la base del triangulo es de:{0}", trian.BaseTriang);
            Console.WriteLine("La altura del triangulo es de:{0}", trian.AlturaTriang);
            Console.WriteLine("El tamaño del area del triangulo es de:{0}", trian.AreaTriang);

            var Rectan = new Rectangulo();
            Rectan.Dathope();
            Console.WriteLine("El nombre de la figura es:{0}", Rectan.NombreFig);
            Console.WriteLine("El tamaño de la base del Rectangulo es de:{0}", Rectan.BaseRec);
            Console.WriteLine("La altura del rectangulo es de:{0}", Rectan.AlturaRec);
            Console.WriteLine("El tamaño del area del Rectangulo es de:{0}", Rectan.AreaRec);

            var Circle = new Circulo();
            Circle.Dathope();
            Console.WriteLine("El nombre de la figura es:{0}", Circle.NombreFig);
            Console.WriteLine("El tamaño del radio del Circulo es de:{0}", Circle.RadioCir);
            Console.WriteLine("El tamaño del area del Circulo es de:{0}", Circle.AreaCir);


        }
    }
