# Rectangle46

NUnit Code -->

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using SENG8040_Assignment1;
using NUnit.Framework;

namespace Rectangle46Test
{
    [TestFixture]
    class RectTest
    {
        [Test]
        public void GetRectangleLength_Input7_Returns7()
        {
            //Arrange
            int length1 = 7;
            int width1 = 0;
            int expectedOutcome = length1;
            Rectangle46 testRect = new Rectangle46(length1, width1);

            //Act
            int actualOutcome = testRect.GetLength();

            //Assert
            Assert.AreEqual(expectedOutcome, actualOutcome);
        }

        [Test]
        public void SetRectangleLength_Input9_Returns9()
        {
            //Arrange
            int length1 = 9;
            int width1 = 0;
            int expectedOutcome = length1;
            Rectangle46 testRect = new Rectangle46(length1, width1);

            //Act
            int actualOutcome = testRect.SetLength(length1);

            //Assert
            Assert.AreEqual(expectedOutcome, actualOutcome);
        }

        [Test]
        public void GetRectangleWidth_Input5_Returns5()
        {
            //Arrange
            int length1 = 0;
            int width1 = 5;
            int expectedOutcome = width1;
            Rectangle46 testRect = new Rectangle46(length1, width1);

            //Act
            int actualOutcome = testRect.GetWidth();

            //Assert
            Assert.AreEqual(expectedOutcome, actualOutcome);
        }

        [Test]
        public void SetRectangleWidth_Input2_Returns2()
        {
            //Arrange
            int length1 = 0;
            int width1 = 2;
            int expectedOutcome = width1;
            Rectangle46 testRect = new Rectangle46(length1, width1);

            //Act
            int actualOutcome = testRect.SetWidth(width1);

            //Assert
            Assert.AreEqual(expectedOutcome, actualOutcome);
        }

        [Test]
        public void GetRectanglePerimeter_Input22and7_Return58()
        {
            //Arrange
            int length1 = 22;
            int width1 = 7;
            int expectedOutcome = (2*(length1 + width1));
            Rectangle46 testRect = new Rectangle46(length1, width1);

            //Act
            int actualOutcome = testRect.GetPerimeter();

            //Assert
            Assert.AreEqual(expectedOutcome, actualOutcome);
        }

        [Test]
        public void GetRectangleArea_Input30and7_Return210()
        {
            //Arrange
            int length1 = 30;
            int width1 = 7;
            int expectedOutcome = length1 * width1;
            Rectangle46 testRect = new Rectangle46(length1, width1);

            //Act
            int actualOutcome = testRect.GetArea();

            //Assert
            Assert.AreEqual(expectedOutcome, actualOutcome);
        }

    }
}
