# Moveis-puma
Transformamos ideias em móveis planejados sob medida, unindo beleza, funcionalidade e qualidade. Criamos soluções personalizadas para cozinhas, quartos, escritórios e mais, com atenção a cada detalhe. Seu espaço com o estilo que você sonha. Fale com a gente!
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;

@Controller
public class VisitCounterController {

    private int visitCount = 0;

    @GetMapping("/")
    public String home(Model model) {
        visitCount++;
        model.addAttribute("visitCount", visitCount);
        model.addAttribute("telefone", "(11) 91234-5678");
        return "index"; // Vai renderizar index.html ou index.jsp
    }
}
