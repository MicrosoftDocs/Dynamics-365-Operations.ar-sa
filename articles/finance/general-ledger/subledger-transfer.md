---
title: تحويل دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام
description: يصف هذا الموضوع القدرات في Microsoft Dynamics 365 Finance المرتبطة بعمليه التحويل بدفتر الأستاذ الفرعي في دفتر الأستاذ العام.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: aec68b9389ee2ef28e8119087392ac5f18ec5dd2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204775"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="4e07b-103">تحويل دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="4e07b-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e07b-104">يصف هذا الموضوع القدرات في Microsoft Dynamics 365 Finance المرتبطة بقواعد تحويل مجموعات من إدخالات دفتر يوميه بدفتر الأستاذ الفرعي.</span><span class="sxs-lookup"><span data-stu-id="4e07b-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="4e07b-105">في الإصدار 8.1، تم إجراء تغييرات للسماح بنقل القواعد، التي أهملت الخيار **متزامن**.</span><span class="sxs-lookup"><span data-stu-id="4e07b-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="4e07b-106">للحصول على مزيد من المعلومات راجع [الميزات المهلكة أو التي تمت إزالتها لـ Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="4e07b-106">For more information, see [Removed or deprecated features for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="4e07b-107">تتوفر الخيارات التالية لنقل مجموعات بدفتر الأستاذ الفرعي.</span><span class="sxs-lookup"><span data-stu-id="4e07b-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="4e07b-108">غير متزامن-سيقوم هذا الخيار علي الفور بجدوله تحويل إدخالات المحاسبة بدفتر الأستاذ الفرعي إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="4e07b-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="4e07b-109">سيتم تسجيل إيصال دفتر الأستاذ العام بمجرد ان تكون الموارد حره لمعالجه هذا الطلب علي الخادم.</span><span class="sxs-lookup"><span data-stu-id="4e07b-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="4e07b-110">المجموعة المجدولة-سيقوم هذا الخيار باضافه الإدخالات المحاسبية لدفتر الأستاذ الفرعي التي يتم تحويلها إلى قائمه انتظار المعالجة في دفتر الأستاذ العام ، حيث ستتم معالجه الإدخالات بالترتيب الذي تم استلامه.</span><span class="sxs-lookup"><span data-stu-id="4e07b-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="4e07b-111">سيتم تسجيل إيصال دفتر الأستاذ العام في الوقت المجدول إذا كانت الموارد حره لمعالجه وظيفة الدفعة هذه علي الخادم.</span><span class="sxs-lookup"><span data-stu-id="4e07b-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="4e07b-112">في إصدار 10.0.8، تم اجراء تحسينات لتحسين أداء الخيار غير المتزامن.</span><span class="sxs-lookup"><span data-stu-id="4e07b-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="4e07b-113">يتم تمكين هذه الميزة ضمن اسم الميزة **تحسين أداء تحويل دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام**.</span><span class="sxs-lookup"><span data-stu-id="4e07b-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="4e07b-114">تعمل هذه الوظيفة علي تحسين نقل البيانات من دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="4e07b-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="4e07b-115">وهو يسمح بان تكون العملية أكثر فعاليه ، كما انها تقوم بتجميع مجموعات من الحركات الأصغر لنقلها.</span><span class="sxs-lookup"><span data-stu-id="4e07b-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="4e07b-116">وهذا يسمح باستخدام خادم المجموعة بكفاءة أكبر.</span><span class="sxs-lookup"><span data-stu-id="4e07b-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="4e07b-117">تتطلب هذه الوظيفة اعداد خادم المجموعة والاتصال بالإنترنت لكي يعمل خيار التحويل غير المتزامن.</span><span class="sxs-lookup"><span data-stu-id="4e07b-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]