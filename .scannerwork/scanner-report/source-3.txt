package fibo;

import static org.junit.Assert.*;

import org.junit.Test;

public class fibonacciTest {

	@Test
	public void testGenerateSeriesCount() {
		int arrayCount = 10;
		int[] series = Fibonacci.generateSeries(arrayCount);
		assertTrue(series.length == arrayCount);
	}

	@Test
	public void testGenerateSeriesMinValue() {
		int arrayCount = 1;
		int[] series = Fibonacci.generateSeries(arrayCount);
		assertTrue(series[0] == 0);
	}

	@Test
	public void testGenerateSeriesValues() {
		int arrayCount = 10;
		int[] series = Fibonacci.generateSeries(arrayCount);
		assertTrue(series[0] == 0);
		assertTrue(series[1] == 1);
		assertTrue(series[2] == 1);
		assertTrue(series[3] == 2);
	}

	@Test
	public void testGenerateSeriesMaxValue() {
		int arrayCount = 10;
		int[] series = Fibonacci.generateSeries(arrayCount);
		assertTrue(series[9] == 34);
	}

	@Test
	public void testGenerateSeriesLimit() {
		int arrayCount = 48;
		int[] series = Fibonacci.generateSeries(arrayCount);
		assertTrue(series[46] > 0);

	}
}
