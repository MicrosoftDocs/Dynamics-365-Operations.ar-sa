---
title: تعطيل القواعد في مدقق تناسق حركات البيع بالتجزئة
description: يصف هذا الموضوع وظيفة تعطيل قواعد مدقق تناسق الحركات في Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: abd97819d44963d22269efc9536f746c3c0b3812
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230580"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="09caa-103">تعطيل القواعد في مدقق تناسق حركات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="09caa-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09caa-104">قد توجد سيناريوهات وعمليات فريدة لدى بائعي التجزئة.</span><span class="sxs-lookup"><span data-stu-id="09caa-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="09caa-105">وبالتالي، لا تنطبق جميع القواعد المضمنة بشكل افتراضي في مدقق تناسق حركة التجارة على جميع بائعي التجزئة.</span><span class="sxs-lookup"><span data-stu-id="09caa-105">Therefore, not all the rules that are included by default in the commerce transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="09caa-106">ولاستيعاب الاختلافات، يقدم Microsoft Dynamics 365 Commerce وظيفة يمكن استخدامها لتعطيل القواعد غير القابلة للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="09caa-106">To accommodate differences, Microsoft Dynamics 365 Commerce provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="09caa-107">لعرض قائمة بالقواعد المتوفرة في مدقق تناسق الحركة في بيئتك، وللاطلاع على حالة كل قاعدة، انتقل إلى **Retail وCommerce \> إعداد Headquarters \> المعلمات \> معلمات Commerce**، وحدد علامة التبويب **التحقق من صحة الحركات‬**.</span><span class="sxs-lookup"><span data-stu-id="09caa-107">To view the list of rules that are available in the transaction consistency checker in your environment, and to see the status of each rule, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="09caa-108">بشكل افتراضي، تكون حالة كل قاعدة معينة إلى **ممكّن**.</span><span class="sxs-lookup"><span data-stu-id="09caa-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="09caa-109">وبالتالي، تُستخدم جميع القواعد للتحقق من صحة الحركات قبل سحبها إلى كشوف حسابات التجارة.</span><span class="sxs-lookup"><span data-stu-id="09caa-109">Therefore, all the rules are used to validate transactions before they are pulled into the commerce statements.</span></span> <span data-ttu-id="09caa-110">لتعطيل قاعدة، يمكنك تغيير حالتها إلى **معطّل**.</span><span class="sxs-lookup"><span data-stu-id="09caa-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="09caa-111">لا تؤخذ القواعد المعطّلة في الاعتبار عندما يتم التحقق من صحة الحركات أثناء عملية حساب كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="09caa-111">Disabled rules aren't considered when transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="09caa-112">لتجاوز عملية التحقق من الصحة بكاملها، بصرف النظر عما إذا كانت القواعد ممكّنة، انتقل إلى **Retail وCommerce \> إعداد Headquarters \> المعلمات \> معلمات Commerce**، ثم في علامة التبويب **التحقق من صحة الحركات‬**، قم بتعيين الخيار **تعطيل مدقق التوافق لحركات Commerce** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="09caa-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Commerce transactions** option to **Yes**.</span></span> <span data-ttu-id="09caa-113">بعد تعيين هذا الخيار إلى **لا**، لا يمكن إعادته إلى **لا** من واجهه المستخدم.</span><span class="sxs-lookup"><span data-stu-id="09caa-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]