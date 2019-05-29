# Rectangle46

Methods -->

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace SENG8040_Assignment1
{
    public class Rectangle46
    {
        private int length;
        private int width;
        
        public Rectangle46()
        {
            length = 1;
            width = 1;
        }

        public Rectangle46(int length, int width)
        {
            this.length = length;
            this.width = width;
        }

        public int GetLength()
        {
            return length;
        }

        public int SetLength(int length)
        {
            this.length = length;
            return this.length;
        }

        public int GetWidth()
        {
            return width;
        }

        public int SetWidth(int width)
        {
            this.width = width;
            return this.width;
        }

        public int GetPerimeter()
        {
            return ((2*(length + width)));
        }

        public int GetArea()
        {
            return ((width * length));
        }
    }
}
