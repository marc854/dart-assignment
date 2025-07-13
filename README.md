#void main() {
  // 1. Define Variables
  int myInt = 42;
  double myDouble = 3.14;
  String myString = "Hello Dart";
  bool myBool = true;
  List<int> myList = [1, 2, 3, 4, 5];

  print("Int: $myInt");
  print("Double: $myDouble");
  print("String: $myString");
  print("Bool: $myBool");
  print("List<int>: $myList");

  // 2. Type Conversion
  print("\nString to Int and Double:");
  print(stringToInt("123"));
  print(stringToDouble("45.67"));

  print("\nInt to String and Double:");
  print(intToString(100));
  print(intToDouble(100));

  // 3. Conversion Function
  print("\nconvertAndDisplay:");
  convertAndDisplay("150");

  // 4. Control Flow
  print("\nIf-Else: Positive/Negative/Zero");
  checkNumber(0);

  print("\nVoting Eligibility:");
  checkVotingEligibility(20);

  print("\nSwitch Case - Day of the Week:");
  printDay(4);

  print("\nFor Loop: 1 to 10");
  for (int i = 1; i <= 10; i++) {
    print(i);
  }

  print("\nWhile Loop: 10 to 1");
  int j = 10;
  while (j >= 1) {
    print(j);
    j--;
  }

  print("\nDo-While Loop: 1 to 5");
  int k = 1;
  do {
    print(k);
    k++;
  } while (k <= 5);

  // 5. Combine Data & Control Flow
  print("\nIterate List, Check Even/Odd & Categorize:");
  List<int> numbers = [3, 25, 120, 7, 88];
  for (var num in numbers) {
    print("Number: $num");
    print(num % 2 == 0 ? "Even" : "Odd");

    switch (true) {
      case true when (num >= 1 && num <= 10):
        print("Small");
        break;
      case true when (num >= 11 && num <= 100):
        print("Medium");
        break;
      case true when (num >= 101):
        print("Large");
        break;
      default:
        print("Invalid");
    }
    print("----");
  }
}

// --- Type Conversion Functions ---

int stringToInt(String s) => int.parse(s);

double stringToDouble(String s) => double.parse(s);

String intToString(int n) => n.toString();

double intToDouble(int n) => n.toDouble();

// --- Convert and Display ---

void convertAndDisplay(String number) {
  int intValue = int.parse(number);
  double doubleValue = double.parse(number);

  print("Int value: $intValue");
  print("Double value: $doubleValue");
}

// --- Control Flow Functions ---

void checkNumber(int num) {
  if (num > 0) {
    print("Positive");
  } else if (num < 0) {
    print("Negative");
  } else {
    print("Zero");
  }
}

void checkVotingEligibility(int age) {
  if (age >= 18) {
    print("Eligible to vote");
  } else {
    print("Not eligible to vote");
  }
}

void printDay(int day) {
  switch (day) {
    case 1:
      print("Monday");
      break;
    case 2:
      print("Tuesday");
      break;
    case 3:
      print("Wednesday");
      break;
    case 4:
      print("Thursday");
      break;
    case 5:
      print("Friday");
      break;
    case 6:
      print("Saturday");
      break;
    case 7:
      print("Sunday");
      break;
    default:
      print("Invalid day");
  }
}
 dart-assignment
