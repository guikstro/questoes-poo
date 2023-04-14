package questões;

import java.awt.*;
import java.awt.event.*;
import javax.swing.*;

public class Q8 extends JFrame implements ActionListener {

    private static final long serialVersionUID = 1L;
    private int numberToGuess;
    private int remainingAttempts;
    private JTextField attemptsTextField;
    private JButton[] numberButtons;

    public Q8() {
        super("Guess Number Game");
        setLayout(new BorderLayout());

        // Gerando número aleatório
        numberToGuess = (int) (Math.random() * 20 + 1);

        // Criando painel para os botões dos números
        JPanel numbersPanel = new JPanel(new GridLayout(4, 5));
        numberButtons = new JButton[20];
        for (int i = 0; i < 20; i++) {
            numberButtons[i] = new JButton("" + (i + 1));
            numberButtons[i].addActionListener(this);
            numbersPanel.add(numberButtons[i]);
        }

        // Criando painel para o contador de tentativas
        JPanel attemptsPanel = new JPanel(new FlowLayout());
        JLabel attemptsLabel = new JLabel("Remaining attempts:");
        attemptsTextField = new JTextField(2);
        attemptsTextField.setEditable(false);
        attemptsTextField.setText("5");
        attemptsPanel.add(attemptsLabel);
        attemptsPanel.add(attemptsTextField);

        // Adicionando os painéis à janela principal
        add(numbersPanel, BorderLayout.CENTER);
        add(attemptsPanel, BorderLayout.SOUTH);

        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setSize(300, 200);
        setLocationRelativeTo(null);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent event) {
        String buttonLabel = event.getActionCommand();
        int guess = Integer.parseInt(buttonLabel);

        // Verificando se o usuário acertou o número
        if (guess == numberToGuess) {
            JOptionPane.showMessageDialog(this, "You guessed the number! Congratulations!");
            System.exit(0);
        } else {
            remainingAttempts--;
            attemptsTextField.setText("" + remainingAttempts);

            if (remainingAttempts == 0) {
                JOptionPane.showMessageDialog(this, "You failed to guess the number. The number was " + numberToGuess);
                System.exit(0);
            } else {
                JOptionPane.showMessageDialog(this, "Sorry, wrong guess. Try again!");
            }
        }
    }

    public static void main(String[] args) {
        new Q8();
    }

}
