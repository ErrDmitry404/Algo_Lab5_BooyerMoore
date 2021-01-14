# Algo_Lab5_BooyerMoore
Algorithm Boyer-Moore

(Алгоритм для пошуку шаблону у стрічці)
{BoyerMoore} class finds the first occurrence of a pattern string in a text string.

Files below:

src contains:
BoyerMoore

tests contains:
BooyerMooreTest

And pom.xml included

How to run:
First you need to check your maven dependencies, and then open tests and run them:
There are two types of tests included with realisation of search:

	@Before
	public void beforeSearch() {
		boyerMoore = new BoyerMoore("AAAGTT");
	}
	
	@Test
	public void testSearchSuccess() {
		assertEquals(0, boyerMoore.search("AAAGTT"));
		assertEquals(1, boyerMoore.search("CAAAGTT"));
		assertEquals(0, boyerMoore.search("AAAGTTC"));
		assertEquals(5, boyerMoore.search("AAAGTAAAGTTAAAGT"));

		System.out.println("!");

	}
	@Test
	public void testSearchFailure() {
		assertEquals(-1, boyerMoore.search("AAAGTC"));
		assertEquals(-1, boyerMoore.search("CAAGTT"));
		assertEquals(-1, boyerMoore.search("AAACTT"));
		assertEquals(-1, boyerMoore.search("AACGTT"));
	}
	
}

also you can run tests using:
mvn test

If code runs without errors - everything allright!

Сlass BoyerMoore
Contains all the methods of search!
