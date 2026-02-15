You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "aboutus.html",
    "context": {
      "title": "DERIVATIVES IT SERVICES PVT LTD | CONSULTING | DEPLOYMENT | TRAINING",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "careers.html",
    "context": {
      "title": "DERIVATIVES IT SERVICES PVT LTD | CONSULTING | DEPLOYMENT | TRAINING",
      "first_heading": "CAREERS"
    }
  },
  {
    "path": "consulting.html",
    "context": {
      "title": "DERIVATIVES IT SERVICES PVT LTD | CONSULTING | DEPLOYMENT | TRAINING",
      "first_heading": "CONSULTING"
    }
  },
  {
    "path": "contactus.html",
    "context": {
      "title": "DERIVATIVES IT SERVICES PVT LTD | CONSULTING | DEPLOYMENT | TRAINING",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/09faef9d128e68cf650bcc9fee5f4b5c.css",
    "context": {
      "path": "css/09faef9d128e68cf650bcc9fee5f4b5c.css"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/3d711e1ca0fa06af86ddcd23e9f1f31a.css",
    "context": {
      "path": "css/3d711e1ca0fa06af86ddcd23e9f1f31a.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/923d7a12989d8629b2276bcb808c92b9.css",
    "context": {
      "path": "css/923d7a12989d8629b2276bcb808c92b9.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "deployment.html",
    "context": {
      "title": "DERIVATIVES IT SERVICES PVT LTD | CONSULTING | DEPLOYMENT | TRAINING",
      "first_heading": "DEPLOYMENT"
    }
  },
  {
    "path": "imgs/048ff0c35618e8779a45cd0d2ed08d71.webp",
    "context": {
      "refs": [
        {
          "alt": "m",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/242f0b06e05a2e765252399bebb93a07.webp",
    "context": {
      "refs": [
        {
          "alt": "Our expertise",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2cff3298b7015f93e703b634d74a9746.webp",
    "context": {
      "refs": [
        {
          "alt": "CONSULTING",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/328d29e2ada51510db9a8953d723d702.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/543b1fae94ff474321a830ce6b080e3b.webp",
    "context": {
      "refs": [
        {
          "alt": "IVT GROUP OF COMPANIES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6777d969bb1113a3b53078d22fbd7d61.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/74e6aad87f4cbf786f0b9a5d3366529d.webp",
    "context": {
      "refs": [
        {
          "alt": "OUR GOALS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/762780481c84c486b99f22c4494af92e.webp",
    "context": {
      "refs": [
        {
          "alt": "ml",
          "title": ""
        },
        {
          "alt": "ml",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/86b9548d7b88845f2c9b0a7f439f26e2.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b62dc26c9449d0c5d9cfeb1c8270fafb.webp",
    "context": {
      "refs": [
        {
          "alt": "OUR MISSION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/be48f18ffedc97aab5e8d7797099923f.webp",
    "context": {
      "refs": [
        {
          "alt": "banner",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/def3baba42c945d37d0bdb7e0a920bda.webp",
    "context": {
      "refs": [
        {
          "alt": "N. Shanmugasundaram",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/df281cab301fe6abc48481decba4dd7e.webp",
    "context": {
      "refs": [
        {
          "alt": "TRAINING",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb3f39164d44d2d2b6298f460223b072.webp",
    "context": {
      "refs": [
        {
          "alt": "DEPLOYMENT",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0415ac668694ed7c9eeb2f63c4c96db.webp",
    "context": {
      "refs": [
        {
          "alt": "l",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "DERIVATIVES IT SERVICES PVT LTD | CONSULTING | DEPLOYMENT | TRAINING",
      "first_heading": "DERIVATIVES IT SERVICES PVT LTD"
    }
  },
  {
    "path": "js/024c2427a07d4754d082b32ff6f47796.js",
    "context": {
      "path": "js/024c2427a07d4754d082b32ff6f47796.js"
    }
  },
  {
    "path": "js/027151cf1be95681de1b467942001858.js",
    "context": {
      "path": "js/027151cf1be95681de1b467942001858.js"
    }
  },
  {
    "path": "js/20ebc5f4fff22d9c0b0df7a66b7d8c8a.js",
    "context": {
      "path": "js/20ebc5f4fff22d9c0b0df7a66b7d8c8a.js"
    }
  },
  {
    "path": "js/2d36e9fa24b491802cf18f39a308190c.js",
    "context": {
      "path": "js/2d36e9fa24b491802cf18f39a308190c.js"
    }
  },
  {
    "path": "js/2d62c5e761d3e1992478716162667ce5.js",
    "context": {
      "path": "js/2d62c5e761d3e1992478716162667ce5.js"
    }
  },
  {
    "path": "js/328ee378638a24926abf5dec969f9194.js",
    "context": {
      "path": "js/328ee378638a24926abf5dec969f9194.js"
    }
  },
  {
    "path": "js/3e734a79111d3ae5022fadd97f4b4570.js",
    "context": {
      "path": "js/3e734a79111d3ae5022fadd97f4b4570.js"
    }
  },
  {
    "path": "js/3f434054cfbcb9efddefc25bf53a0b2b.js",
    "context": {
      "path": "js/3f434054cfbcb9efddefc25bf53a0b2b.js"
    }
  },
  {
    "path": "js/425f5d74616f0950ab7f6aa8a2ba3011.js",
    "context": {
      "path": "js/425f5d74616f0950ab7f6aa8a2ba3011.js"
    }
  },
  {
    "path": "js/4a184d88eb9269b7dbce11b716f40379.js",
    "context": {
      "path": "js/4a184d88eb9269b7dbce11b716f40379.js"
    }
  },
  {
    "path": "js/56848c032b05f79a1c67ea6d7b451252.js",
    "context": {
      "path": "js/56848c032b05f79a1c67ea6d7b451252.js"
    }
  },
  {
    "path": "js/5cd7f03eb032ff5d1a79d9daad244677.js",
    "context": {
      "path": "js/5cd7f03eb032ff5d1a79d9daad244677.js"
    }
  },
  {
    "path": "js/61ce9c6e209c2c6687f8b2e0bb0fa78f.js",
    "context": {
      "path": "js/61ce9c6e209c2c6687f8b2e0bb0fa78f.js"
    }
  },
  {
    "path": "js/6432203ce192bdda9fff6890193487b5.js",
    "context": {
      "path": "js/6432203ce192bdda9fff6890193487b5.js"
    }
  },
  {
    "path": "js/7b9a1dfa2ba7ebd6966eb4b5a2b8cccf.js",
    "context": {
      "path": "js/7b9a1dfa2ba7ebd6966eb4b5a2b8cccf.js"
    }
  },
  {
    "path": "js/7d7d8ec406a653220337bde42ddcd998.js",
    "context": {
      "path": "js/7d7d8ec406a653220337bde42ddcd998.js"
    }
  },
  {
    "path": "js/969912c5e1cdd73b7812defd4dbd0119.js",
    "context": {
      "path": "js/969912c5e1cdd73b7812defd4dbd0119.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a626b42d5e9f3bebfd9624955f0d721b.js",
    "context": {
      "path": "js/a626b42d5e9f3bebfd9624955f0d721b.js"
    }
  },
  {
    "path": "js/aeea5981f09059b3304ead8b513e8042.js",
    "context": {
      "path": "js/aeea5981f09059b3304ead8b513e8042.js"
    }
  },
  {
    "path": "js/afe09ede095ecb21a7d57d52891fbfe8.js",
    "context": {
      "path": "js/afe09ede095ecb21a7d57d52891fbfe8.js"
    }
  },
  {
    "path": "js/bd271374cbdbf6b93a861a0d1da4d44b.js",
    "context": {
      "path": "js/bd271374cbdbf6b93a861a0d1da4d44b.js"
    }
  },
  {
    "path": "js/c0a73d949973f41fdb7cb5098a95c51d.js",
    "context": {
      "path": "js/c0a73d949973f41fdb7cb5098a95c51d.js"
    }
  },
  {
    "path": "js/d1ec9a5167f878e894e5532ac741f0dd.js",
    "context": {
      "path": "js/d1ec9a5167f878e894e5532ac741f0dd.js"
    }
  },
  {
    "path": "js/d2a524fa5eb75b486a06e4ccd15439a7.js",
    "context": {
      "path": "js/d2a524fa5eb75b486a06e4ccd15439a7.js"
    }
  },
  {
    "path": "js/d352e2eabcb455f640e092975e9b5946.js",
    "context": {
      "path": "js/d352e2eabcb455f640e092975e9b5946.js"
    }
  },
  {
    "path": "js/e83b51d598b2a45483252c3be82d77b0.js",
    "context": {
      "path": "js/e83b51d598b2a45483252c3be82d77b0.js"
    }
  },
  {
    "path": "js/f17632f1cc1088a1c285f0d8e9cedde0.js",
    "context": {
      "path": "js/f17632f1cc1088a1c285f0d8e9cedde0.js"
    }
  },
  {
    "path": "js/f5b6708cffe7c1147c483017fbec7d58.js",
    "context": {
      "path": "js/f5b6708cffe7c1147c483017fbec7d58.js"
    }
  },
  {
    "path": "training.html",
    "context": {
      "title": "DERIVATIVES IT SERVICES PVT LTD | CONSULTING | DEPLOYMENT | TRAINING",
      "first_heading": "TRAINING"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.