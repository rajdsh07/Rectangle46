# Rectangle46
Get Length &amp; Width Program
public int GetPerimeter()
        {
            return ((2*(length + width)));
        }
        


public int GetArea()
        {
            return ((width * length));
        }

       [Test]
        public void GetRectanglePerimeter_Input22point0and7point0_Return58point0()
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
        public void GetRectangleArea_Input30point0and7point0_Return210point0()
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

