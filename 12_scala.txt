import scala.io.StdIn

object SimpleCalculator {
  def main(args: Array[String]): Unit = {
    println("Welcome to Simple Calculator!")
    println("Please enter the first number:")
    val num1 = StdIn.readLine().toDouble

    println("Please enter the second number:")
    val num2 = StdIn.readLine().toDouble

    println("Select operation:")
    println("1. Addition")
    println("2. Subtraction")
    println("3. Multiplication")
    println("4. Division")

    val choice = StdIn.readInt()

    val result = choice match {
      case 1 => num1 + num2
      case 2 => num1 - num2
      case 3 => num1 * num2
      case 4 => if (num2 != 0) num1 / num2 else "Cannot divide by zero"
      case _ => "Invalid choice"
    }

    println(s"Result: $result")
  }
}
